# DSx_Backflush
Backflush Plugin for the [famous DSx skin by Damian](https://www.diy.brakel.com.au/dsx/) (v4.38 or later) on Decent Espresso machines (https://github.com/decentespresso and https://decentespresso.com/)

This plugin helps to automate backflushing by running a dedicated pressure profile and restoring all previous settings afterwards.

## Installation:

1. save `DSx_backflush.dsx` file to skins/DSx/DSx_Plugins
2. make sure, you have a Backflush.tcl profile (e.g. the one proposed [by Stéphane in Decent Diaspora customers forum](https://3.basecamp.com/3671212/buckets/7351439/messages/2940917783#__recording_2959508002)); file name matters, so make sure to spell it correctly
3. restart DE1 app

## Usage:

1. place blind basket into PF and lock it in group head
2. press "Backflush" text above favorite cups
3. on GHC press espresso button (non GHC machines should start directly but I could not test this)
4. after the backflush is completed (or canceled) your former profile is reloaded

## Known issues:

1. profile name color and fav cup indicators don't change when running backflush
2. Restore of unsaved profiles (e.g. temperature adjustment) after backflush restores to original profile and discards unsaved changes
