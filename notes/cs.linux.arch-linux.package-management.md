---
id: 7ngmc0jelxou2f0h0jv1mc6
title: Package Management
desc: ''
updated: 1709471063794
created: 1709470702217
---

### Check for package cache

Pacman stores its downloaded packages in `/var/cache/pacman/pkg/` and does not remove the old or uninstalled versions automatically. This has some advantages:

- It allows to downgrade a package without the need to retrieve the previous version through other means, such as the Arch Linux Archive.
- A package that has been uninstalled can easily be reinstalled directly from the cache directory, not requiring a new download from the repository.

**Cleaning the cache:**

- Read more here : https://wiki.archlinux.org/title/pacman#Cleaning_the_package_cache


The paccache(8) script, provided within the pacman-contrib package, deletes all cached versions of installed and uninstalled packages, except for the most recent three, by default: 

```bash
paccache -r
```