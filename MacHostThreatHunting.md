# Explore File Download [T1546.016](https://attack.mitre.org/techniques/T1546/016) [T1027.006](https://attack.mitre.org/techniques/T1027/006) [T1566.002](https://attack.mitre.org/techniques/T1566/002) [T1218.001](https://attack.mitre.org/techniques/T1218/001) [T1189](https://attack.mitre.org/techniques/T1189) [T1203](https://attack.mitre.org/techniques/T1203)[T1608.004](https://attack.mitre.org/techniques/T1608/004) [T1218.005](https://attack.mitre.org/techniques/T1218/005) [T1204.001](https://attack.mitre.org/techniques/T1204/001) [T1176](https://attack.mitre.org/techniques/T1176) [T1185](https://attack.mitre.org/techniques/T1185)
1. Look within Downloads.plist within ```~/Library/Safari```. 
2. Look at History.db within ```~/Library/Safari``` and use the safari_history.txt module within [APOLLO](https://github.com/mac4n6/APOLLO/blob/master/modules/safari_history.txt). 

# View Safari History [T1189](https://attack.mitre.org/techniques/T1189) [T1203](https://attack.mitre.org/techniques/T1203)[T1608.004](https://attack.mitre.org/techniques/T1608/004) [T1218.001](https://attack.mitre.org/techniques/T1218/001) [T1218.005](https://attack.mitre.org/techniques/T1218/005) [T1204.001](https://attack.mitre.org/techniques/T1204/001) [T1176](https://attack.mitre.org/techniques/T1176) [T1185](https://attack.mitre.org/techniques/T1185)
1. Look at History.db within ```~/Library/Safari``` and use the safari_history.txt module within [APOLLO](https://github.com/mac4n6/APOLLO/blob/master/modules/safari_history.txt). 
2. Use [mac_apt](https://github.com/ydkhatri/mac_apt) to parse Safari history with ```python3 mac_apt.py DD /home/ubuntu/[name of image].img SAFARI -c -o /home/ubuntu/evidence/``` and look for the DOWNLOAD event in the output csv. 

# View Chrome History [T1189](https://attack.mitre.org/techniques/T1189) [T1203](https://attack.mitre.org/techniques/T1203)[T1608.004](https://attack.mitre.org/techniques/T1608/004) [T1218.001](https://attack.mitre.org/techniques/T1218/001) [T1218.005](https://attack.mitre.org/techniques/T1218/005) [T1204.001](https://attack.mitre.org/techniques/T1204/001) [T1176](https://attack.mitre.org/techniques/T1176) [T1185](https://attack.mitre.org/techniques/T1185)
1. View ```~/Library/Application\ Support/Google/Chrome/Default``` for the History.db. 

# View Installed Programs [T1543](https://attack.mitre.org/techniques/T1543) [T1036.005](https://attack.mitre.org/techniques/T1036/005)[T1569](https://attack.mitre.org/techniques/T1569)
1. Look within ```/Library/Receipts/InstallHistory.plist```. 
2. Use [mac_apt](https://github.com/ydkhatri/mac_apt) with ```python3 mac_apt.py DD /home/ubuntu/[name of image].img INSTALLHISTORY -c -o /home/ubuntu/evidence/installhistory/``` and look for installers!

# Service Permissions [T1543.003](https://attack.mitre.org/techniques/T1543/003/)
1. Look within ```/Library/Application Support/com.apple.TCC/TCC.db``` and use the APOLLO tcc_db.txt. The full list with explanations can be found here [deepdive](https://www.rainforestqa.com/blog/macos-tcc-db-deep-dive#all-services). 
2. Look within ```/Library/Receipts/InstallHistory.plist```. 
3.  Use [mac_apt](https://github.com/ydkhatri/mac_apt) with ```python3 mac_apt.py DD /home/ubuntu/[name of image].img TCC -c -o /home/ubuntu/evidence/tcc/``` to find all permissions. 

# Examine Startup Actions [T1547](https://attack.mitre.org/techniques/T1547/)
1. Look within ```~/Library/LaunchAgents``` for each agents and find the plist files. 
2. Use [mac_apt](https://github.com/ydkhatri/mac_apt) with ```python3 mac_apt.py DD /home/ubuntu/[name of image].img AUTOSTART -c -o /home/ubuntu/evidence/autostart/``` to find lauch agents. 

# File Download [T1546.016](https://attack.mitre.org/techniques/T1546/016) [T1027.006](https://attack.mitre.org/techniques/T1027/006) [T1566.002](https://attack.mitre.org/techniques/T1566/002) [T1218.001](https://attack.mitre.org/techniques/T1218/001) [T1189](https://attack.mitre.org/techniques/T1189) [T1203](https://attack.mitre.org/techniques/T1203)[T1608.004](https://attack.mitre.org/techniques/T1608/004) [T1218.005](https://attack.mitre.org/techniques/T1218/005) [T1204.001](https://attack.mitre.org/techniques/T1204/001) [T1176](https://attack.mitre.org/techniques/T1176) [T1185](https://attack.mitre.org/techniques/T1185)
1. Use [mac_apt](https://github.com/ydkhatri/mac_apt) to parse Safari history with ```python3 mac_apt.py DD /home/ubuntu/[name of image].img SAFARI -c -o /home/ubuntu/evidence/``` and look for the DOWNLOAD event in the output csv. 

# Find Malicious Installers [T1546.016](https://attack.mitre.org/techniques/T1546/016/)
1. Use [mac_apt](https://github.com/ydkhatri/mac_apt) to parse recent items with  ```python3 mac_apt.py DD /home/ubuntu/[name of image].img RECENTITEMS -c -o /home/ubuntu/evidence/recentitems``` and look for recent documents. 
2. Look within ```/Library/Receipts/InstallHistory.plist```. 

# Examine Launch Agents Persistence [T1543.001](https://attack.mitre.org/techniques/T1543/001/)
1. Use [mac_apt](https://github.com/ydkhatri/mac_apt) with ```python3 mac_apt.py DD /home/ubuntu/[name of image].img AUTOSTART -c -o /home/ubuntu/evidence/autostart/``` to find lauch agents. 
2. Look within ```~/Library/LaunchAgents``` for each agents and find the plist files. 