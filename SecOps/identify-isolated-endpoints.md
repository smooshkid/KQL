# Identify isolated endpoints

## Description

The following query will return endpoints which have been isolated by looking into relevant registry modifications.

### Microsoft Defender XDR
```
DeviceRegistryEvents
| where ActionType == "RegistryValueSet"
| where RegistryKey == @"HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Advanced Threat Protection"
| where RegistryValueType == "Dword"
| where RegistryValueName == "DisableEnterpriseAuthProxyValueToRestoreAfterIsolation"
| where RegistryValueData == "1"
| where PreviousRegistryValueName == "DisableEnterpriseAuthProxyValueToRestoreAfterIsolation"
| project Timestamp, DeviceId, DeviceName
```
