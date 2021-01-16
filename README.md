wsconfig is an ansible playbook that initially sets up or updates configuration of (fedora) Linux workstations in an easily reproducible way. It might help to keep the same configuration on a bunch of machines or on the only one. It can do:
- copy .dotfiles/config. The files supposed to be in separate/private repo - 'filesrepo' inventory var (the repo's 'home' dir will be synced then with target's '~' dir, as well as 'etc' with '/etc/')
- install apps - packages and flatpaks
- configure GNOME, including setting a desktop wallpaper, selecting favourite apps and their order in the dash/dock.
\
\
Usage:
```bash
$ git clone ...
$ cd wsconfig
$ vim hosts

$ ansible-playbook -i ./hosts apply.yml
```
