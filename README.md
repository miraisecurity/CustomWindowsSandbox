# CustomWindowsSandbox
This project is to demonstrate how you can customize the built-in Windows Sandbox to have software pre-installed every time you boot up the sandbox. This can be useful for a clean test bed or if you are like me, prefer not to install every teleconferencing software under the sun.

# Original Proof of Concept Setup
There is a WSB file that when double clicked (in windows) will launch the sandbox, I usually place this on my desktop. There are several configuration options you can apply to this config file, See: https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-sandbox/windows-sandbox-configure-using-wsb-file

Within this WSB configuration you can execute a file or script. I found it only wanted to execute one command, therefore I had it execute a batch file instead.

The batch file contain several instructions. First it copies over the pre-downloaded installation files (Zoom, Webex, TorBrowser, etc) and then runs silent installations.

Within about 30 seconds, I have a clean sandbox with the various software I need and good audio and video pass through

# Future Opportunities
Ideally, we would want this script to download the newest versions of whatever software you want to install. This is likely something to add to a new version of the batch file. You can create several different Custom Sandboxes through creating different batch files and then creating a new WSB file for each profile.
