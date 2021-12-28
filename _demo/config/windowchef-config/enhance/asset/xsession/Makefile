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
	@echo '	$$ make install'
	@echo
	@echo '	$$ make remove'
	@echo

.PHONY: help


install: xsession-install config-install
.PHONY: install

xsession-install:
	sudo install -Dm644 ./xsessions/windowchef-session.desktop /usr/share/xsessions/windowchef-session.desktop
	sudo install -Dm755 ./xsessions/windowchef-session /usr/share/windowchef/xsessions/windowchef-session
.PHONY: xsession-install

config-install:
	sudo install -Dm644 ./config/windowchef/environment /usr/share/windowchef/config/windowchef/environment
	sudo install -Dm755 ./config/windowchef/autostart /usr/share/windowchef/config/windowchef/autostart
.PHONY: config-install




remove: xsession-remove config-remove
.PHONY: remove

xsession-remove:
	sudo rm -f /usr/share/xsessions/windowchef-session.desktop
	sudo rm -f /usr/share/windowchef/xsessions/windowchef-session
.PHONY: xsession-remove

config-remove:
	sudo rm -f /usr/share/windowchef/config/windowchef/environment
	sudo rm -f /usr/share/windowchef/config/windowchef/autostart
.PHONY: config-remove
