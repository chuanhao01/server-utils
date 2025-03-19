PATH_TO_USER_HOME = /home/$(USER)

# Help Commands
.PHONY: default
default: help

# Main Commands
.PHONY: install
install:
	if [ -f $(PATH_TO_USER_HOME)/.gitconfig ]; then \
		cp $(PATH_TO_USER_HOME)/.gitconfig $(PATH_TO_USER_HOME)/.gitconfig.bak; \
	fi
	ln -srf gitconfig $(PATH_TO_USER_HOME)/.gitconfig

	if [ -f $(PATH_TO_USER_HOME)/.config/git ]; then \
		cp $(PATH_TO_USER_HOME)/.config/git $(PATH_TO_USER_HOME)/.config/git-bak; \
	fi
	mkdir -p $(PATH_TO_USER_HOME)/.config
	ln -srf git $(PATH_TO_USER_HOME)/.config/git

.PHONY: remove-check
remove-check:
	rm $(PATH_TO_USER_HOME)/.gitconfig
	rm -r $(PATH_TO_USER_HOME)/.config/git


.PHONY: help
help:
	@echo 'Please make sure the user listed below is correct'
	@echo 'User: $(USER)'
	@echo ''
	@echo 'PLEASE READ THE README.md before running any commands'
	@echo 'Usage: make [command]'
	@echo 'install - Install configs using symlinks'
	@echo 'remove-check - Remove .gitconfig and .config/git'
