# TV guide + playlists

**Guide (EPG):** `all.xml` — 34 channels, rebuilt and pushed nightly.

**Playlists:** attach these in Televizo on the TCL.

| File | Channels |
|---|---|
| `CCTV-17ch.m3u` | 17 CCTV channels |
| `WORLDNEWS-4ch.m3u` | CNN, ABC News Live, BBC News, NHK World-Japan |
| `EASTASIA-3ch.m3u` | TTV News, TTV, FTV |

## Setup on the TCL

Televizo -> menu -> Playlist -> "+" -> **URL** (not FILE) -> paste:

```
https://raw.githubusercontent.com/boonkwee396/tv-guide/main/CCTV-17ch.m3u
https://raw.githubusercontent.com/boonkwee396/tv-guide/main/WORLDNEWS-4ch.m3u
https://raw.githubusercontent.com/boonkwee396/tv-guide/main/EASTASIA-3ch.m3u
```

The programme guide imports itself from each playlist's header. It uses two
of Televizo's two free EPG slots:

```
CCTV 1-17         https://live.fanmingming.com/e.xml
everything else   https://raw.githubusercontent.com/boonkwee396/tv-guide/main/all.xml
```

If titles are missing, add those two in Televizo -> Settings -> EPG and turn
OFF every other entry. A full slot limit fails silently.
