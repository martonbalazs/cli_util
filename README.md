cli_util
=============

Simple utils

A selection of handy CLI utilities.

* cpucsekk hangs until the CPU usage drops below 15% and no I/O requests are queuing for the internal drive. I don't like overloading the system by starting a lot of things together. (Credits go to Paul Colby.) The one named silent_cpucsekk does what you'd guess. Threshold % levels (default: 15%) can be set in the txt files of ~/.cpucsekk (plain numbers and nothing else there, please).

* daddybank [input file] [optional currency] is a utility to keep track of kids' pocket money. It needs an input file with lines of the format:
`<orgmode style active date> [name] [currency] [set/add/sub/int/yrl] [amount] [whatever comment from here]`
e.g. `<2017-03-19 Sun> John GBP set 56.45`
where [name] must be a single word, and the fourth entry is any of
 * `set` to set balance,
 * `add` to add to balance,
 * `sub` to subtract from balance,
 * `int` to set interest rate in %/year for account,
 * `yrl` to set yearly premium for account.

 Multiple names in distinct lines are supported and result in separate accounts. Lines starting with # are ignored. The script adds `yrl/365` daily to the account and also adds daily compounded interest `int/(100*365)` based on the daily balance. `int` and `yrl` can be set multiple times with different dates. An optional currency code as a second parameter to the script triggers a conversion rate download from ECB and combines all accounts of a [name] into the desired currency. 

* datumhom prints the date (yy.mm.dd), time, and weather. Uses metar for weather, thus needs it installed as well as an airport (and its ICAO code) nearby. Refresh intervals can also be set, see the script itself. It has been designed to use with the gltext screensaver. 

* dbst hangs until Dropbox says "Idle" three times with 1 sec differences. I use it to make sure no other synchronization script starts before Dropbox finishes. 

* itterminal opens yet another terminal in the current directory. Simple, but needed a million times.

* mypubip emails you your public ip if it has changed. This is my replacement for dyndns; can be run every few minutes using crontab. :-) See the script for settings. The one named ecmypubip doesn't send email, just echoes your public ip if changed.

* picrndv opens a random directory from your photalbum (a dir to be given as parameter). I run it once a day. :-)

* reteti [integer] [optional text] (**re**peating **te**rminal **ti**mer) reminds you via zenity and a system sound about "text" every "integer" minutes.

I'm no programmer, so please don't blame me on the quality of the code. :-)

Licensed under GNU GPLv3.
