# LanLens releases

Signed updates for **LanLens**, a Mac app that shows every device on your home
network, who's home, internet health and security.

LanLens checks this repository once a day and installs new versions from inside
the app, with no download and no reinstall.

## How updates stay safe

- `latest.json` (at the top) says which version is current and where to get it.
  Each version's files live in `updates/<version>/`, including
  `lanlens-code-<version>.zip` (the update itself).
- Both are signed with the LanLens release key. LanLens refuses any update that
  isn't signed with that key, or whose files don't match their signed
  fingerprints, even if someone changes the files here.
- An update that fails to start twice is set aside automatically, and LanLens
  goes back to the last version that worked.

The signing key is never stored in this repository.
