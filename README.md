# Path-of-Exile
The goal is to optimization and improvement PoE, and finde the best settings for running fast, for heavy content or players with lower end pc's

<details>
<summary>All linkes to sources of information</summary>

An PoE players 2021 guide https://www.pathofexile.com/forum/view-thread/2730973 <br/>
Launch options https://www.poewiki.net/wiki/Launch_options <br/>
General https://www.ghostarrow.com/path-of-exile-increase-fps-performance <br/>
Notepad++ download https://notepad-plus-plus.org/downloads/ <br/>
</details>


<details>
<summary>Launch options</summary>
There is a guide in the link on how to applay the lunche options. <br />
https://www.poewiki.net/wiki/Launch_options

### Use the following
#
    --nologo
Disables the animated intro along with the sound.

#
    --waitforpreload
Wait for preloading to finish during startup.
This causes the game to not finish the initial loading screen until it has fully loaded,
all of the stuff that would otherwise be background-loaded during the first moments of play.

### Consider using
#
    -gc 2
The number of generations to keep around when running garbage collection.
While this feature fixes out of memory (EOUTOFMEMORY or Unable to Map File),
crashes it significantly increases loading time between zones.

#
    --softwareaudio
Forces use of generic software audio device.
Fixes a bug with Creative sound cards causing game crashes.

### How to apply on desktop version
#
    "...\Path of Exile\Client.exe" --nologo --waitforpreload --softwareaudio -gc 2

</details>


<details>
<summary>Production Config</summary>
To my current knowledge, path of exile is using an old sound engine, reasulting in it costing a lot of performance.
    
#
    production_Config.ini
1: To fix this first finde the production config.

#
    Right click and select properties, under the General tab, Click the box "Read-only"
2: Make the file read-only

#
    master_volume2            = xx
    ambient_sound_volume2     = flase
    dialogue_sound_volume2    = false
    sound_effects_volume2     = false
    music_volume2             = false
    chat_alert_sound_volume   = xx
    reverb_enabled2           = false
    item_filter_sound_volume2 = xx
    mute_in_background        = false
    channel_count             = low or medium
    disable_char_events       = true
3: Edit the file, xx = anyvalue 0-100. (I use notepad++) <br/><br/>
### (Spacing is only to help the reader of the github)
</details>

<details>
<summary>Extra options</summary>
    
#
    bloom_strength = 0
Turn off bloom in the production_Config.ini file. (not sure if 0 or false is best)

#
    "...\Path of Exile\PathOfExile_x64.exe"
Use the 64bit luncher, the luncher is at the download location.
</details>
