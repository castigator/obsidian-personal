---
tags:
  - hosting
---

## Hosting Archive

Everything on [[DreamHost]] that wasn't a live site was archived in October 2026, then moved to Google Drive. Back to [[Hosting]].

- **Where:** Google Drive (rupertthomas@gmail.com) → My Drive → **Hosting Archives**. `MANIFEST.tsv` there lists every archive with its source folder, file counts and size.
- **How it was checked:** each archive's file count matched the server's. The Drive copies' sizes were checked against the manifest through the Drive API.
- **Warning:** some archives contain old malware (e.g. `*.INFECTED.php` in the old pebmarsh.com `blog.old`, leftovers in thecodecollective). Google Drive may flag them. Never upload their contents to a web server.

### What's in the Big Ones

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

### Status (28 Oct 2026)

- **39 archives in Drive and verified:** their folders have been deleted from DreamHost.
- **`home-data.tar`, `home-archive.tar.gz` and `home-Backups.tar.gz`:** verified in Drive, and `~/data`, `~/archive` and `~/Backups` deleted from DreamHost on 2 Nov 2026 (home folder 29 GB → 2.5 GB). Only `~/archive/mindseye` remains. Local copies on the Mac deleted 2 Nov 2026; Drive is the only copy.
- **Uploaded 30 Oct 2026, re-verified 1 Nov:** Drive for desktop couldn't upload them, so they went up with rclone in 1 GiB parts to Drive "Hosting Archives/dreamhost-home-2026-10" (27 parts; every part's md5 matches the local copy). The folder also holds `PARTS.md5`, `MANIFEST.tsv` (sha256 of each whole archive) and `REJOIN.txt` (how to rebuild them). Entry counts match the server for `~/data` (1,129) and `~/Backups` (69,501). `~/archive` matches except `~/archive/mindseye`, left out because an old deleted user owns it; it was archived separately on 2 Nov 2026 as `home-archive-mindseye.tar.gz` (95 MB, 1,516 of 1,519 entries; `logs/` and `.bash_history` were unreadable). Uploads go through the Drive for desktop folder only: no rclone on the work Mac (its security team queried it). Local copies are in `~/Downloads/dreamhost-archive-2026-10` on the Mac.
- **`www-pebmarsh-honeycode.pebmarsh.com.tar.gz` (209 MB, 29 Oct 2026):** the honeycode site folder, including `downloads/` (33 APK/DMG files, versions 1.0.0–1.6.0). All 85 files checksum-verified against the server before the folder was deleted. Also waiting to upload.
- **`www-pebmarsh-wp.pebmarsh.com.tar.gz` (71 MB, 30 Oct 2026):** the old pebmarsh.com WordPress folder (13,085 entries) plus a dump of `wp_pebmarsh_com`. In Drive with a matching md5 and listed in `MANIFEST.tsv`. Contains the SEO-spam malware found 30 Oct ([[Incident 2026-10 Backdoor]]), kept as evidence: don't restore it. Folder and database deleted from DreamHost 1 Nov 2026.
- **Deleted without keeping a copy** (Rupert's decision): `~/trash`, `wp-school.pebmarsh.com` and `wp-school.pebmarsh.com.old`.
- **Can't be deleted by the account:** `~/stuart.pebmarsh.com` (75 MB of 2009 Acrobat help files, uid 30070, not archived) and `~/archive/mindseye` (uid 15274, archived 2 Nov 2026). No ticket: they go when the DreamHost account closes.
- **July 2026 clean-up material:** the databases of dead sites (church, next.pebmarsh.com, the old blog, villagehall, stopwaterlane) are in `home-db-archive-2026-07.tar.gz`; the incident evidence is in `home-incident-2026-07-17.tar.gz`. A local copy is in `~/Downloads/dreamhost-backups-2026-07` on the Mac, with the July disk-cleanup report.
