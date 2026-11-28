# Marka releases

This repository contains release binaries and update metadata for **Marka**, a
local-first Windows assessment system for Philippine schools and review centers.

**The Marka source repository is private and is not published here.** This
repository contains no source code, build scripts, certificates, private keys,
databases, or learner records.

## Latest: 0.2.9

- Installer: `MarkaSetup-0.2.9.exe`
- Size: 80,568,032 bytes (about 80.5 MB)
- SHA-256: `29d5a5fb2bbbb679b0b0973acd9117632a393de6d8a3f71fc7dc90f998de23ae`

0.2.9 simplifies the app and website UI, removes redundant descriptions, fixes
dashboard and mock-exam context switching, refreshes screenshots, and improves
accessibility. Existing installations should update through the app's **Check
for updates** action.

Download from the **Releases** tab. The `manifest.json` file at the repository
root is the update channel used by the desktop app.

## Verify the download

```powershell
Get-FileHash .\MarkaSetup-0.2.9.exe -Algorithm SHA256
```

Compare the result with `SHA256SUMS.txt` and the hash in `manifest.json`. If the
hash does not match, do not run the installer.

## Installer signature

The installer is signed with the Marka private CA (`CN=Marka`). A Windows PC
that does not trust the current root may show an unknown-publisher or SmartScreen
warning. The SHA-256 is the integrity check. School IT can deploy the current
`MarkaRootCA.cer` to managed devices; request the public certificate and
deployment notes through the issue tracker at
https://github.com/justlurking-around/marka-releases/issues. The current root is
`CDEFFA7C22F2E62C63AE5F017E81E57B50709BF7`; 0.2.6 used a different root.

## License

Proprietary. See [LICENSE](LICENSE). No source code is provided. Use of the
software is governed by the Marka End User License Agreement supplied with the
installer. Redistribution of modified binaries is not permitted.
