---
tags:
  - hosting
---

# Hosting Archive

Everything on [[DreamHost]] that wasn't a live site was archived in October 2026, then moved to Google Drive. Back to [[Hosting]].

- **Where:** Google Drive (rupertthomas@gmail.com) → My Drive → **Hosting Archives**. `MANIFEST.tsv` there lists every archive with its source folder, file counts and size.
- **How it was checked:** each archive's file count matched the server's. The Drive copies' sizes were checked against the manifest through the Drive API.
- **Warning:** some archives contain old malware (e.g. `*.INFECTED.php` in the old pebmarsh.com `blog.old`, leftovers in thecodecollective). Google Drive may flag them. Never upload their contents to a web server.

## What's in the big ones

- **`home-data.tar` (9.5 GB):** family photos and videos from 2007–08: Daisy's 7th birthday, Dylan's birthday and Mallorca, Cala D'or 2007, Christmas 2007 and more. 833 photos and 211 `.avi` videos.
- **`home-archive.tar.gz` (8.4 GB):**
  - `transfer_from_heathen`: the old hosting server's web folder, with Mind's Eye client sites.
  - `svn`: Subversion repositories (cc, personal, clients, conchango).
  - `backup/maple_one`: a machine backup.
  - Old sites: skinningthecat, quizwinner, fundowl and others.
  - Disc images and installers.
- **`home-Backups.tar.gz` (7.0 GB):**
  - Server backups from 2007.
  - A Virgin backup (`takeme.zip`, an Outlook `.pst`).
  - An old PC's dev and cygwin folders.
  - The Code Collective Ltd QuickBooks books (2002).
  - ICS client documents.

## Status (28 Oct 2026)

- **39 archives in Drive and verified:** their folders have been deleted from DreamHost.
- **3 still uploading or unverified:** `home-data.tar`, `home-archive.tar.gz` and `home-Backups.tar.gz`. Once they're verified, delete `~/data`, `~/archive` and `~/Backups` from DreamHost.
- **29 Oct 2026: still not in the cloud.** Google's side shows 0 bytes for all three. Drive for desktop keeps logging `UNAVAILABLE_WHILE_OFFLINE` although the Mac is online, and a second copy of `home-Backups.tar.gz` (7.5 GB) is in Drive's `lost_and_found`. The Mac's disk is 97% full (17 GB free), which may be a factor. The local copies are complete and readable. Check the cloud size before deleting anything on DreamHost; never sign out of Drive while uploads are pending.
- **`www-pebmarsh-honeycode.pebmarsh.com.tar.gz` (209 MB, 29 Oct 2026):** the honeycode site folder, including `downloads/` (33 APK/DMG files, versions 1.0.0–1.6.0). All 85 files checksum-verified against the server before the folder was deleted. Also waiting to upload.
- **Deleted without keeping a copy** (Rupert's decision): `~/trash`, `wp-school.pebmarsh.com` and `wp-school.pebmarsh.com.old`.
- **Can't be deleted by the account; needs a DreamHost ticket:** `~/stuart.pebmarsh.com` (75 MB of 2009 Acrobat help files, uid 30070) and `~/archive/mindseye` (uid 15274). Neither was archived.
- **July 2026 clean-up material:** the databases of dead sites (church, next.pebmarsh.com, the old blog, villagehall, stopwaterlane) are in `home-db-archive-2026-07.tar.gz`; the incident evidence is in `home-incident-2026-07-17.tar.gz`. A local copy is in `~/Downloads/dreamhost-backups-2026-07` on the Mac, with the July disk-cleanup report.
