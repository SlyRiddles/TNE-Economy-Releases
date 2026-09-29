# TNE-Economy releases

Official compiled plugin downloads for Paper and Folia. Download the latest TNE-Economy jar from [Releases](https://github.com/SlyRiddles/TNE-Economy-Releases/releases/latest).

TNE-Economy 1.0.6 and newer download verified updates directly from this repository and install them on a normal server restart. The source code remains in a separate private repository. No GitHub token is required by server owners.

Each release includes the jar, a SHA-256 checksum and tne-economy-latest.json used by the updater.

## Live update notifications

TNE-Economy 1.0.8+ connects to TNECORE 1.0.11+ for live release signals. Publishing a stable release runs the **Notify Minecraft servers** workflow, which wakes connected plugins through TNECORE. Owners see current/newest versions and a restart instruction after the verified download. The workflow can also be run manually after upgrading TNECORE.

The signal contains no release instructions or credentials. Plugins independently verify this repository's latest manifest and JAR. Periodic checks remain available if the live connection is unavailable. Source commits without a published JAR do not announce an installable update.
