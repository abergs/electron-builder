---
"app-builder-lib": patch
---

fix(mac): correctly handle MAS signing and afterSign hook timing

Fixed MAS builds using wrong provisioning profile by skipping signing in `signApp()` and letting `pack()` handle it with correct MAS options. The `afterSign` hook now fires at the correct time - after the app is actually signed with MAS options, not after incorrect darwin signing.
