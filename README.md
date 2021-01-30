# DSx_Backflush
Backflush Plugin for the [famous DSx skin by Damian](https://www.diy.brakel.com.au/dsx/) (v4.38 or later) on Decent Espresso machines (https://github.com/decentespresso and https://decentespresso.com/)

This plugin helps to automate backflushing by running a dedicated pressure profile and restoring all previous settings afterwards.

## Installation:

1. save `DSx_backflush.dsx` file to skins/DSx/DSx_Plugins
2. make sure, you have a Backflush.tcl profile (e.g. the one proposed [by Stéphane in Decent Diaspora customers forum](https://3.basecamp.com/3671212/buckets/7351439/messages/2940917783#__recording_2959508002)); file name matters, so make sure to spell it correctly or make sure to set another file name using configuration (see below)
3. restart DE1 app

## Usage:

1. place blind basket into PF and lock it in group head
2. press "Backflush" text above favorite cups
3. on GHC press espresso button (non GHC machines should start directly but I could not test this)
4. after the backflush is completed (or canceled) your former profile is reloaded

## Configuration (optional):

DSx_Backflush provides different configuration options: 

- you can place the "Backflush" UI element in the top left corner of DSx main screen (for example because you have another plugin running, that needs the space just above the favourite cups)
- you can change the label of the UI element in idle and running state
- you can chose the profile filename to use
- you can bypass shot history 

All of those configurtaions can be set using a text editor to change (some of) the first five lines in the plugin file. For example you can place a "Clean" UI element in the top left corner, that starts the Weber Spring Clean profile and saves it's run in shot history like this:

    set ::DSx_BF_alternative_ui 1
    set ::DSx_BF_label_idle "Clean"
    set ::DSx_BF_label_active "Cleaning ..."
    set ::DSx_BF_profile_filename "weber_spring_clean"
    set ::DSx_BF_bypass_shot_history 0

Default values are:

    set ::DSx_BF_alternative_ui 0
    set ::DSx_BF_label_idle "Backflush"
    set ::DSx_BF_label_active "Backflushing ..."
    set ::DSx_BF_profile_filename "Backflush"
    set ::DSx_BF_bypass_shot_history 1

## Known issues:

1. profile name color and fav cup indicators don't change when running backflush
2. Restore of unsaved profiles (e.g. temperature adjustment) after backflush restores to original profile and discards unsaved changes
