# Issue Title: User Cannot Connect to Wi-Fi

# Problem Scenario
User reports they cannot connect to Wi-Fi on a Windows 10 laptop. Other users are able to connect successfully.

#  Environment
- Device: Dell laptop (Windows 10 Pro)
- Network: Office Wi-Fi (DHCP enabled)
- User role: Standard domain user

# Troubleshooting Steps
1. Confirmed wireless toggle was ON  
2. Checked list of available networks – Wi-Fi not showing  
3. Ran `ipconfig` — no active adapter  
4. Restarted network adapter via Device Manager  
5. Verified adapter driver was enabled  
6. Confirmed IP assignment from DHCP  
7. Connected successfully to network

# Root Cause
Network adapter was disabled after a system update.

# Resolution
Re-enabled adapter and reconnected user to the network.

# Prevention / Recommendation
- Educate users on safely shutting down PC during updates
- Monitor drivers after patch installations

# Tools Used
- Device Manager
- ipconfig / ping
- Windows Network Troubleshooter

### 📸 Screenshot
![WiFi Screenshot](./screenshot_wifi.png)


# Key Skills Demonstrated
- Windows OS troubleshooting
- Basic networking understanding
- Customer communication
