# How I Fixed Pearson OnVUE System Testing Problems (Mac)!

I encountered issues during the system check before my online exam on Pearson OnVUE. Given the difficulty of reaching technical support and the fact that many problems have persisted despite years of complaints, I want to share what finally worked for me when troubleshooting the system test on a Mac:

## System test: Diagnostics - Network check 80%
Video streaming connection error

    Video streaming connection results and requirements:    
    Your home/office network failed to connect to the required video streaming service.  
    The streaming connection requires that Wowza.com can be reached as well as a stable connection of at least 1mb upload and download speeds.    
    How to connect to our video streaming service:    
    Contact your network administrators and ensure the following:    
    Any network filtering software is disabled  
    WebRTC WebSocket connections must be allowed to *.*.cloud.wowza.com on TCP port 80, 443, 1935.

If you're sure your Mac's firewall settings and router are properly configured, the issue may be that the Access Code has expired. 
In that case, you can request a new one. 
How? Simply follow the link in the confirmation email to test your system, and from there, you’ll be able to generate a new code.

![Lint to test your system](https://github.com/VaHiX/notes/blob/3307f9a7e51afb28d9f18dc1af6d5a90f29fa0b4/Images/OnVUE/email.png?raw=true)

## System test - Exam simulation - Secure browser test
If you've already completed official three steps:
 - Press Command + Option + Escape and close all applications except for Finder and OnVUE.
 - Only one monitor is allowed. Please unplug any extra monitors.
 - Do not use a corporate network or VPN.

You can try the following additional troubleshooting steps:
- Clear BrowserLock:
	- Run the command: `rm -rf ~/.BrowserLock/`
- Disable Stage Manager:
	- Go to System Settings > Desktop & Dock > Stage Manager and toggle it off.
- Grant OnVUE 'Input Monitoring' Permission:
	- Go to Privacy & Security > Input Monitoring, click the + sign, and add the OnVUE app.
	- You can also toggle off permissions for other apps, like Logi Options+, that aren't OnVUE.

And finally, my last tricky step:
Enable **Open using Rosetta** for OnVUE.

![Open using Rosetta](https://github.com/VaHiX/notes/blob/5af4401176e1d7b1ea4ca264fd313472b262d060/Images/OnVUE/rosetta.png?raw=true)
