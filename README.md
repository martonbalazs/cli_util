cli_util
=============

Simple utils

A selection of handy CLI utilities.

- cpucsekk hangs until the CPU usage drops below 30% and no I/O requests are
  queuing for the internal drive. I don't like overloading the system by
  starting a lot of things together. (Credits go to Paul Colby.) The one named
  silent_cpucsekk does what you'd guess.

- datumhom prints the date (yy.mm.dd), time, and weather. Uses metar for
  weather, thus needs it installed as well as an airport (and its ICAO code)
  nearby. Refresh intervals can also be set, see the script itself. It has been
  designed to use with the gltext screensaver. 

- dbst hangs until Dropbox says "Idle" three times with 1 sec differences. I
  use it to make sure no other synchronization script starts before Dropbox
  finishes. 

- itterminal opens yet another terminal in the current directory. Simple, but
  needed a million times.

- mypubip emails you your public ip if it has changed. This is my replacement
  for dyndns; can be run every few minutes using crontab. :-) See the script
  for settings. The one named ecmypubip doesn't send email, just echoes your
  public ip if changed.

- reteti [integer] [optional text] (**re**peating **te**rminal **ti**mer)
  reminds you via zenity and a system sound about "text" every "integer"
  minutes.

I'm no programmer, so please don't blame me on the quality of the code. :-)
Licensed under GNU GPLv3.
