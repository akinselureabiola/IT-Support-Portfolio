# Issue Title: Browser Not Loading Websites / Internet Browsing Failure

# Problem Scenario
A user reports that outlook website are not loading properly in Internet Explorer. Pages timeout or show certificate errors, while other users are unaffected.

# Environment
- Windows 10/11 workstation
- Browser: Chrome/Edge/Firefox
- Network: Wi-Fi or LAN
- DNS: DHCP or Google DNS

# Troubleshooting Steps Performed
1. Confirmed internet connectivity using command line:
- ping outlook.com
- ping google.com
2. Tried accessing multiple websites to rule out site outage
3. Cleared browser cache, cookies, and history
4. Disabled problematic extensions and ad blockers
5. Reset browser settings to default
6. Flushed DNS cache using:
- ipconfig /flushdns
7. Tested resolving websites using:
- nslookup google.com
8. Tested site in another browser
9. Temporarily disabled proxy/VPN settings
10. Rebooted computer and browser

# Root Cause
The problem was that the virtual machine uses Internet Explorer that cannot work with the present web applications like Outlook.com.
The site would not load properly due to the old browser engine that was used by the IE and also because of the stringent security policies that the browser enforced. 

# Resolution
Cleared cache, flushed DNS, disabled extensions but the problem was solved with the installation of a modern browser (Google Chrome) and gave access.

# Prevention & Recommendations
- Periodically clear cached data
- Avoid installing untrusted extensions
- Restart browser/computer regularly
- Use modern browsers and auto-update

# Tools Used
- Internet Explorer
- Chrome settings panel
- Command Prompt (ping, nslookup, ipconfig)
- Browser extensions manager
- Network settings

# Skills Demonstrated
- Network troubleshooting
- Browser diagnostics
- DNS understanding
- Practical step-by-step problem solving
- User communication
