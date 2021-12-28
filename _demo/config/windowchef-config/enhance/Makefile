default: help
.PHONY: default

help:
	@echo 'Usage:'
	@echo '	$$ make [action]'
	@echo
	@echo 'Example:'
	@echo '	$$ make'
	@echo '	$$ make help'
	@echo
	@echo '	$$ make clone'
	@echo
	@echo '	$$ make prepare-arch-build'
	@echo
	@echo '	$$ make build'
	@echo
	@echo '	$$ make install'
	@echo
	@echo '	$$ make remove'
	@echo

.PHONY: help


install: windowchef-install xsession-install config-install
.PHONY: install

remove: windowchef-remove xsession-remove config-remove
.PHONY: remove


##
## * https://aur.archlinux.org/packages/?K=windowchef
## * https://aur.archlinux.org/packages/windowchef/
## * https://aur.archlinux.org/cgit/aur.git/tree/PKGBUILD?h=windowchef
## * https://aur.archlinux.org/packages/windowchef-git/
## * https://aur.archlinux.org/cgit/aur.git/tree/PKGBUILD?h=windowchef-git
##

prepare-arch-build:
	sudo pacman -Sy --needed libxcb xcb-util-wm xcb-util-keysyms
.PHONY: prepare-arch-build

clone:
	git clone https://github.com/tudurom/windowchef.git src/windowchef
.PHONY: clone

build:
	make -C src/windowchef
.PHONY: build

windowchef-install: build
#	sudo install -Dm755 ./src/windowchef/windowchef /usr/bin/windowchef
	sudo install -Dm755 ./src/windowchef/windowchef /usr/local/bin/windowchef
#	sudo install -Dm755 ./src/windowchef/waitron /usr/bin/waitron
	sudo install -Dm755 ./src/windowchef/waitron /usr/local/bin/waitron
.PHONY: windowchef-install


windowchef-remove:
#	sudo rm -f /usr/bin/windowchef
	sudo rm -f /usr/local/bin/windowchef
#	sudo rm -f /usr/bin/waitron
	sudo rm -f /usr/local/bin/waitron
.PHONY: windowchef-remove




xsession-install:
	make -C ./asset/xsession install
.PHONY: xsession-install

xsession-remove:
	make -C ./asset/xsession remove
.PHONY: xsession-remove




config-install:
	make -C ./asset/config install
.PHONY: config-install

config-remove:
	make -C ./asset/config remove
.PHONY: config-remove
