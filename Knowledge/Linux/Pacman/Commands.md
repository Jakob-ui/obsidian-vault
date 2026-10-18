### Remove a Package
- `pacman -R package_name_`

#### Remove a Package and its dependencies
- `pacman -Rs _package_name_`

#### Remove unnecessary dependencies
- `pacman -Qdtq | pacman -Rs -`

#### Upgrading packages
- `pacman -Syu`

#### Installing local or third-party packages
- `pacman -U http://www.example.com/repo/example.pkg.tar.xz`