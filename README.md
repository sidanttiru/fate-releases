# FATE Windows releases

This repository distributes FATE installers and signed update metadata for testing.
Application source is maintained separately. This temporary update source will move
to the advisor-owned repository through a verified transition for existing installations.

Download `FATE-Setup.exe` from the latest release and install it once on each Windows
computer that will run FATE. Subsequent releases are available through the installed
dashboard's **Check for updates**, **Download update**, and **Update and restart** controls.

Each release contains:

- `FATE-Setup.exe`, containing the application and its private Python runtime
- `update.manifest`, binding the version, installer digest, and compatible upgrade sequence
- `update.sig`, the release signature checked by the installed updater

The release signature is separate from Windows Authenticode publisher signing.
The current installer is not Authenticode-signed and can display a Windows publisher warning.
The private release-signing key is never included in this repository or the installer.

These builds require final installed and actual-firewall testing. Release notes describe
the verified scope and remaining limitations. Application updates preserve protected
settings, credentials, and audit history. Any required data compatibility steps appear
in the dashboard after restart.
