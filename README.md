# Marka releases

This repository contains release binaries and update metadata for **Marka**, a
local-first Windows assessment system for Philippine schools and review centers.

**The Marka source repository is private and is not published here.** This
repository contains no source code, build scripts, certificates, private keys,
databases, or learner records.

## Latest: 0.2.6

- Installer: `MarkaSetup-0.2.6.exe`
- Size: 80,555,080 bytes (about 80.5 MB)
- SHA-256: `6efb377bb3f63f6c22357ba04874b3736ad5d75eb42f91daf697b9f4dcc26630`

Download from the **Releases** tab. The `manifest.json` file at the repository
root is the update channel used by the desktop app.

## Verify the download

```powershell
Get-FileHash .\MarkaSetup-0.2.4.exe -Algorithm SHA256
```

Compare the result with `SHA256SUMS.txt` and the hash in `manifest.json`. If the
hash does not match, do not run the installer.

## Installer signature

The installer is signed with the Marka private CA (`CN=Marka, O=Marka, C=PH`).
A Windows PC that does not trust that CA may show an unknown-publisher or
SmartScreen warning; it is not a publicly trusted certificate. The SHA-256 is
the integrity check. School IT can deploy the public root and issuing
certificates to managed devices; request them and the GPO/Intune notes through
the issue tracker at
https://github.com/justlurking-around/marka-releases/issues.

## License

Proprietary. See [LICENSE](LICENSE). No source code is provided. Use of the
software is governed by the Marka End User License Agreement supplied with the
installer. Redistribution of modified binaries is not permitted.
