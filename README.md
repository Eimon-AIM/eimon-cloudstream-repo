# Eimon Cloudstream Repo

Public binary releases for Eimon's Cloudstream extensions.

## Add to Cloudstream

Open **Settings → Extensions → Add repository** and enter:

```text
https://raw.githubusercontent.com/Eimon-AIM/eimon-cloudstream-repo/builds/repo.json
```

Repository name: **Eimon Cloudstream Repo**.

## AniKoto

Install **AniKoto** for independent browsing/search, Latest Dubbed/Subbed and movie catalogues, episode lists and playback. **No Phisher or AniKoto Account installation is required.** Series use the Sub/Dub episode selector; movies offer labelled SUB/DUB choices in the player's Sources menu where available.

Standalone AniKoto is now the supported release, following user confirmation of playback and account features. The obsolete **AniKoto Account** extension has been removed from the current listing and its binary is no longer distributed. If it is still installed, remove it manually; repository removal does not uninstall it or migrate its saved login. Disable Phisher's **AniKoto** provider to avoid conflicting provider names.

Public browsing/playback needs no login. For personal lists, open AniKoto's gear/settings, sign in with **Remember me** checked, then select **Use this session**. Standalone AniKoto has its own saved login. Passwords are not stored; session cookies are stored unencrypted in app data, so do not share preferences or backups.

### Account Continue Watching and resume

Compatible **Eimon Android and Windows forks** show account Continue Watching inside AniKoto's own Home rows, with progress and automatic resume at the saved episode/timestamp. These apps are unofficial forks, not official CloudStream releases. Other extensions do not automatically gain this integration. Stock or unsupported hosts retain ordinary account rows as a fallback.

**Watching – New Episodes** checks recent updates against website progress: at least 80% watched and a higher-numbered episode in the same audio edition. Its recent-title scan is bounded, not a complete release tracker.

**AniKoto v3 + Windows 1.0.6-eimon / Android 4.8.0-eimon.2:** series details show cloud episode progress and resume at the saved timestamp. Earlier episodes in the matching season/audio edition are inferred watched in memory, not imported into local history. Future episode spoilers use Windows' existing toggle or Android's episode options. Native New Episodes cards start the newest eligible same-edition episode at **00:00** after fresh validation, without inheriting the old timestamp. Stock and older hosts retain the ordinary extension row. Signed-in Windows playback checks passed; Android automated tests/APK assembly passed, with phone/TV acceptance still pending.

### Optional progress uploads

Uploads remain **off by default**. Enable them explicitly in **Sync / account options**, then reopen a title through AniKoto and use the built-in player. Only newly saved, matched positions are uploaded; old local history is not uploaded. Movies, ambiguous episode matches, external players and casting may not be covered.

The position-based bridge sends periodic/trailing updates, not immediate pause/exit reports. Pending uploads are memory-only; no durable offline queue is included. Avoid simultaneous playback on multiple devices, since local positions can overwrite website progress. Website sessions and mirrors can still expire or fail.

### Session diagnostics (v2)

Version 2 adds **Sync / account options → Session diagnostics** to investigate unexpected sign-outs. It retains a short trace across restarts: UTC timestamps, endpoint categories, HTTP status, authentication-cookie additions/removals/rotation, and recovery outcomes. It does **not** record cookie values/fingerprints, passwords, account IDs, full URLs, response bodies or user agents. No diagnostics are uploaded automatically.

Existing saved login, audio and upload preferences are preserved; no new sign-in is required if your session still works. After updating, restart Cloudstream once to load the new plugin. If the logout happens again, report the session-diagnostics text—not preference files or cookie-store backups. The update helps identify a recurrence; it does not claim to fix website-side token invalidation.

## Qrmzi — قرمزي

Install **Qrmzi** for Turkish series, movies, latest episodes and Arabic search, using the site's available video-server choices. No account or Phisher extension is required. Original HLS masters preserve available audio/subtitle tracks. Version 2 fixes Android's stricter regex parsing; unavailable uploads and broken mirrors cannot be guaranteed.

## Updates

Refresh repositories in Cloudstream to receive **AniKoto v3**. Qrmzi v2 is unchanged and the retired AniKoto Account extension remains excluded. This repository contains binaries and install manifests; source is maintained separately.
