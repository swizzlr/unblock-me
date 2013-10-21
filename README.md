##Unblock-Me
#####*The easiest way to switch between DHCP and Unblock-Us DNS servers.*

###Usage

Reopen your Terminal. Type "unblock-me" to toggle DHCP DNS and Unblock-Us DNS EU servers.

###Requirements
- `pcregrep` (available via [Homebrew](http://brew.sh))

###Known Issues

- Only uses EU unblock-us DNS. Please submit an issue/pull request describing how I should figure out you aren't a socialist, and what a free DNS IP looks like. I'll update it.
- Hardcoded DNS for EU. If this changes the script needs changing.

Unix-ninjas need not read the below, except to know that the script must be run as a super user if you don't want to have to enter passwords in a dialog.

###Installation Part 1
`chmod 755 unblock-me`

Now decide whether you want to have to type in your admin password every time. If you do, follow the masochist route, otherwise, read on.

###Installation Part 2 – Run as root
1. Add this to your .bash_profile (or .bashrc if you want it to run in non-interactive shells...?): `alias unblock-me="sudo /absolute/path/to/unblock-me"`
2. `sudo visudo` and add this to the end: `ALL    ALL = (root) NOPASSWD: /absolute/path/to/unblock-me`

###Installation Part 2 – I hate myself
1. `ln -s /absolute/path/to/unblock-me /usr/local/bin/unblock-me`

###Acknowledgments
Thanks to [Lisa Lueddecke](https://twitter.com/LisaLueddecke) for patiently waiting for me to write this script so we can optimize our Netflix viewing habits. It was totally worth it...?
