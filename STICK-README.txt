TCL TV - IPTV SETUP (thumb drive)
=================================
Everything on this drive works by itself. No account, no login, nothing to type.

FILES - keep these in the ROOT of the drive, not inside a folder
  CCTV-17ch.m3u       17 CCTV channels (中国央视)
  WORLDNEWS-4ch.m3u   CNN | ABC News Live | BBC News | NHK World-Japan
  EASTASIA-3ch.m3u    台視新聞 TTV News | 台視 TTV | 民視 FTV
  README-FIRST.txt    this file

PREFERRED ROUTE (no thumb drive at all)
 If the TV has internet, you don't need this drive. In Televizo choose URL
 instead of FILE and paste:
   https://raw.githubusercontent.com/boonkwee396/tv-guide/main/CCTV-17ch.m3u
   https://raw.githubusercontent.com/boonkwee396/tv-guide/main/WORLDNEWS-4ch.m3u
   https://raw.githubusercontent.com/boonkwee396/tv-guide/main/EASTASIA-3ch.m3u
 Those stay current forever. This drive is the offline fallback.

HOW TO LOAD THEM
 1. Copy all four files to the ROOT of a FAT32 or exFAT thumb drive.
 2. Plug the drive into the TV. Open the TV's FILE MANAGER and open the drive.
    Do NOT type a filename into the browser bar.
 3. Play -> Televizo -> menu -> Playlist -> "+" -> FILE -> pick a .m3u file.
 4. Repeat for the other two. They will show as CCTV / WORLDNEWS / EASTASIA.

PROGRAMME GUIDE (EPG) - TWO entries, exactly the two free slots
 Televizo has 2 EPG slots. These two files use both of them.

   1) CCTV 1-17        - refreshes itself, never expires
      https://live.fanmingming.com/e.xml

   2) everything else  - rebuilt and republished every night at ~07:55 SGT
      https://raw.githubusercontent.com/boonkwee396/tv-guide/main/all.xml

 Both are already in the playlist headers, so Televizo imports them by itself.
 If titles are missing: Televizo -> Settings -> EPG, add those two URLs, and
 turn OFF every other entry in that list. A full slot limit fails SILENTLY,
 which is the usual reason a guide "doesn't work".

NOTHING EXPIRES
 Every channel on this drive has a guide that renews on its own:
   CCTV 1-17 .................. fanmingming, self-refreshing
   CNN / ABC / BBC / NHK ....... nightly rebuild, pushed to GitHub
   台視新聞 / 台視 / 民視 ......... same nightly rebuild
 You should never need to re-copy this drive again.

 IF TITLES EVER STOP (it shouldn't happen)
 The GitHub guide is a snapshot between pushes. If the nightly job stops
 running, titles freeze and then run out about two days later. Channels keep
 playing either way. Re-copying the drive with a fresh build fixes it.

IF A CHANNEL WILL NOT PLAY
 These are public streams of free-to-air channels and they move or die without
 warning. Other channels are unaffected. Ask and they get re-sourced.

NOTE
 Direct-TS channels (台視, 民視) can take a few seconds to start. They are not
 HLS, so they buffer differently. Everything else is HLS.
