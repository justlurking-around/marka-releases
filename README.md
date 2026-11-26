# Marka releases

This repository contains release binaries and update metadata for **Marka**, a
local-first Windows assessment system for Philippine schools and review centers.

**The Marka source repository is private and is not published here.** This
repository contains no source code, build scripts, certificates, private keys,
databases, or learner records.

## Latest: 0.2.4

- Installer: `MarkaSetup-0.2.4.exe`
- Size: 80,545,888 bytes (about 80.5 MB)
- SHA-256: `3dd83210a8bc2f52c0f148ea2e4c2df4bd5b14a50fc59758c3f32c3954f7c428`

Download from the **Releases** tab. The `manifest.json` file at the repository
root is the update channel used by the desktop app.

## Verify the download

```powershell
Get-FileHash .\MarkaSetup-0.2.4.exe -Algorithm SHA256
```

Compare the result with `SHA256SUMS.txt` and the hash in `manifest.json`. If the
hash does not match, do not run the installer.

## Installer signature

The installer is signed with the Marka development certificate (`CN=Marka Dev`).
A Windows PC that does not trust that certificate may show an unknown-publisher
or SmartScreen warning. The SHA-256 is the integrity check. School IT can trust
the Marka certificate for managed devices; request the public `.cer` and
deployment notes through the issue tracker at
https://github.com/justlurking-around/marka-releases/issues.

## License

Proprietary. See [LICENSE](LICENSE). No source code is provided. Use of the
software is governed by the Marka End User License Agreement supplied with the
installer. Redistribution of modified binaries is not permitted.
