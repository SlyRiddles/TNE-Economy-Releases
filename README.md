# TNE-Economy releases

Official compiled plugin downloads for Paper and Folia. Download the latest TNE-Economy jar from [Releases](https://github.com/SlyRiddles/TNE-Economy-Releases/releases/latest).

TNE-Economy 1.0.11 and newer download verified updates directly from this repository and install them on a normal server restart. The source code remains in a separate private repository. No GitHub token is required by server owners.

Each release includes the jar, a SHA-256 checksum and tne-economy-latest.json used by the updater.

## Server status and owner controls (1.0.14)

TNE-Economy 1.0.14 reports Minecraft version and local event counts about every 30 seconds. With TNECORE 1.0.16 and the latest website, the developer server directory uses the installation connection for online status, SQL health, and plugin version.

Server owners can review and submit local balance adjustments, transaction reversals, item/XP deliveries, and failed-delivery recovery from their own server console. Requests are scoped to the owned installation and saved with a stable ID; reconnecting or resending cannot apply them twice. Player targets must be registered locally. Local grants do not issue central TNE backing.

Restart TNECORE to update it, deploy the latest website, then restart Minecraft once the verified plugin update is ready.

## Versioned installed filenames

Starting with 1.0.13, automatic updates install as `TNE-Economy-<version>.jar`. Paper/Folia applies the verified update and renames the old JAR during startup. Older pending TNE downloads are removed while unrelated plugins' updates are preserved.

When upgrading from 1.0.12 or earlier, the old updater initially keeps the old filename. After 1.0.13 starts, wait for **FILENAME UPDATE READY**, then restart once more to correct it. Future updates change the version and filename together in one restart. No TNECORE or website update is needed.

## Install the updater fix once

Versions before 1.0.11 can announce an update but reject downloading it because Paper/Folia reports API `26.1.0` while the manifest uses `26.1`. Version 1.0.11 fixes that comparison.

If you are stuck on an older version, stop Minecraft, replace the existing TNE plugin JAR with the latest release, and start Minecraft. Keep your plugin data/config folder and only one installed TNE JAR. Future compatible updates download automatically and install on restart. With the default Bukkit setting, pending updates go in `plugins/update`; `plugins/TheNewerEconomy/updates` holds state and backups.

## Live update notifications

TNE-Economy 1.0.8+ connects to TNECORE 1.0.11+ for live release signals. Publishing a stable release runs the **Notify Minecraft servers** workflow, which wakes connected plugins through TNECORE. Owners see current/newest versions and a restart instruction after the verified download. The workflow can also be run manually after upgrading TNECORE.

The signal contains no release instructions or credentials. Plugins independently verify this repository's latest manifest and JAR. Periodic checks remain available if the live connection is unavailable. Source commits without a published JAR do not announce an installable update.
