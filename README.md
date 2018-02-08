# bing_bot


Overview
--------
This script allows you to run a random amount of Bing searches, with random 
search terms, waiting a random number of seconds between searches.  The idea 
is to max out your daily [Microsoft Rewards](https://rewards.microsoft.com/) 
points, without ever actually having to use Bing.  Ideally, you would set this 
up to run daily via Windows Task Scheduler or cron job. 

**Enjoy your free XBOX LIVE!**

Requirements
------------
The `bing_bot` script could be easily modified to run on just about anything with bash and a browser.

But here is how I have it working on my machine:

* **Windows 10** 
  * Windows platform is only required for the `taskkill` utility. 
  * Windows 10 is only required for Microsoft Edge.
* **Cygwin** 
  * [Cygwin](https://cygwin.com) is only required for the `cygstart` utility.
  * Packages needed: `jq, curl`
  * Packages can be installed by running the Cygwin `setup.exe`.
* **Microsoft Edge**
  * Microsoft Edge is only required for the extra bonus points.
  * Microsoft Edge should be set as your default browser.
  * You will need to be signed into Bing with your Xbox Live account.
  * I would also advise that you adjust Microsoft Edge browser settings to clear all open tabs when exiting. 
* **Windows Task Scheduler (Optional)**
  * Only required if you want this to run on a daily schedule. 
  * I found this to be the easier option, over trying to get cron jobs working in Cygwin.
  * Just set up a daily task to run: `c:\cygwin64\bin\bash.exe -l -c "/path/to/bing_bot"`

Usage
-----
    ./bing_bot                      Start up the bing_bot with defaults
    ./bing_bot -c [config.json]     Start up the bing_bot with custom config
    ./bing_bot -h                   Display this screen