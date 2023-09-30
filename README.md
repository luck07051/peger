# Peger

Peger is a script that let you manage packages from a file like nixos.

## Install

Just download the script and execute it.

## Usage

```sh
peger [options] [packages list file]
```

Using `peger` without option to use popup terminal for install/uninstall packages.
```sh
peger [packages list file]
```

Adding -g option to use in same terminal, so you can use `peger` without gui.
```sh
peger [packages list file]
```

Recommend to use tool like `entr` for automation.
```sh
echo 'file' | entr -np peger 'file' &
```


The example of the packages list file:
```
# Line with '#' will be ignore.

# The line start with '##' will be execute, so you can specify the install command like:
##install_cmd="pacman -S"
##uninstall_cmd="pacman -Rns"
##get_local_packages_cmd="pacman -Qq"
##terminal_cmd="st -t installer -c float"

# Package list
package1
package2 package3
```
