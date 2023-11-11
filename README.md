# VLCControl.scpt - Control VLC in OS X Terminal

This is a AppleScript for controlling VLC through
Terminal.app.

The scenario for which it was originally designed is controlling VLC,
which is playing on a Mac, via ssh, while working on a Linux computer 
on the other side of the room.

Currently supported functions are: play/pause, next/previous 
track, jumping in time, toggling fullscreen and changing volume.
This pretty much covers everything the AppleScript hooks of VLC
allow.

Tested to work on MacOS Monterey and VLC 3.0.18.
No guarantees.

You may use, adapt, modify etc. any way you want.


## Installation

I am assuming that if you need to control VLC through the terminal 
you know enough about terminal usage.

The simplest way to install the script is just to just download the 
script file from the GitHub page and add the line `alias 
vlc="osascript /path/to/VLCControl.scpt"` in your `.profile`.

If you have `git`, even simpler will be to clone this repository with 
`git clone git://github.com/jeroenbegyn/VLCControl.git` and then edit 
`.profile` as above. This will also make it easy to keep up to date 
with possible updates to the script.


## Usage

* To start VLC playback, type `vlc start` or `vlc play`. 
If you do this locally and VLC is not running, it will start. 
* To pause VLC playback, type `vlc pause`.
* To stop VLC playback, type `vlc stop`.
* To go to the next track, type `vlc next`.
* To go to the previous track, type `vlc previous` or `vlc 
prev`.
* To print information about the currently playing track, 
type `vlc info`
* To jump to a particular time in the track, type `vlc jump N`,
where N is the track position in seconds.
* To fast forward, type `vlc forward N` where N is the number of
seconds to jump ahead.
* To rewind, type `vlc rewind N` where N is the number of
seconds to jump backwards.
* To change volume, type `vlc volume N` where N is a number between
0 and 100.
* To show a list of these commands, just type `vlc`.

### Over SSH

To enable the SSH server on OS X, go to Sharing in the System Preferences
and enable Remote Login. The Sharing screen will also then tell you the
command to use to connect to your Mac in the local network.
