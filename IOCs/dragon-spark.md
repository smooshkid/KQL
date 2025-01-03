## resources:
  https://www.sentinelone.com/labs/dragonspark-attacks-evade-detection-with-sparkrat-and-golang-source-code-interpretation/

## SparkRAT as seen used by DragonSpark
***Malware staging infrastructure***
```
  11.149.237[.]108	            - China	A compromised server hosting web content related to gambling.
  43.129.227[.]159	            - Hong Kong	A Windows Server 2012 R2 instance with a computer name of 172_19_0_3. The threat actors may have obtained access to this server using a shared or bought account. We observed login credentials with the server’s name being shared over different time periods in the Telegram channels King of VP$ and SellerVPS for sharing and/or selling access to virtual private servers.
  www[.]bingoplanet[.]com[.]tw	- Taiwan	A compromised server hosting web content related to gambling. The website resources have been removed at the time of writing. The domain has been co-hosted with several other websites of legitimate business, including travel agencies and an English preschool.
  www[.]moongallery.com[.]tw	  - Taiwan	A compromised server hosting the website of the Taiwanese art gallery Moon Gallery.
  www[.]holybaby.com[.]tw	      - Taiwan	A compromised server hosting the website of the Taiwanese baby product shop retailer Holy Baby.
  13.213.41[.]125	              - Singapore	An Amazon Cloud EC2 instance named EC2AMAZ-4559AU9.
```

***C2 server infrastructure***
```
  103.96.74[.]148	Hong Kong	A Windows Server 2012 R2 instance with a computer name of CLOUD2012R2.
    The threat actors may have obtained access to this server using a shared or bought account. We observed login credentials with the server’s name being shared over different time periods in the Telegram channels Premium Acc, IRANHACKERS, and !Only For Voters for sharing and/or selling access to virtual private servers.
    This set of infrastructure was observed resolving to jiance.ittoken[.]xyz at the time of writing. This specific domain can be linked to a wider set of Chinese phishing infrastructure over the past few years. It is unclear if they are related to this same actor.
  104.233.163[.]190	United States	A Windows Server 2012 R2 instance with a computer name of WIN-CLC0OFDKTMK.
    The most recent passive DNS record related to this IP address points to a domain name with a Chinese TLD – kanmn[.]cn. However, this is shared hosting infrastructure through Aquanx and likely used by a variety of customers.
    This IP address is known to have hosted a Cobalt Strike C2 server and been involved in other malicious activities, such as hosting known malware samples.
```

***Indicators of Compromise***
  ```
  Description	                                  Indicator
  ShellCode_Loader (a PyInstaller package)	        83130d95220bc2ede8645ea1ca4ce9afc4593196
  m6699.exe	                                        14ebbed449ccedac3610618b5265ff803243313d
  SparkRAT	                                        2578efc12941ff481172dd4603b536a3bd322691
  C2 server network endpoint for ShellCode_Loader	  103.96.74[.]148:8899
  C2 server network endpoint for SparkRAT	          103.96.74[.]148[:]6688
  C2 server network endpoint for m6699.exe	        103.96.74[.]148:6699
  C2 server IP address for China Chopper	          104.233.163[.]190
  Staging URL for ShellCode_Loader	                hxxp://211.149.237[.]108:801/py.exe
  Staging URL for m6699.exe                        	hxxp://211.149.237[.]108:801/m6699.exe
  Staging URL for SparkRAT	                        hxxp://43.129.227[.]159:81/c.exe
  Staging URL for GotoHTTP	                        hxxp://13.213.41.125:9001/go.exe
  Staging URL for ShellCode_Loader                	hxxp://www.bingoplanet[.]com[.]tw/images/py.exe
  Staging URL for ShellCode_Loader                	hxxps://www.moongallery.com[.]tw/upload/py.exe
  Staging URL for ShellCode_Loader	                hxxp://www.holybaby.com[.]tw/api/ms.exe
```
