PATH_TO_USER_HOME = /home/$(USER)

# Help Commands
.PHONY: default
default: help

# Main Commands
.PHONY: install
install:
	if [ -f $(PATH_TO_USER_HOME)/.vimrc ]; then \
		cp $(PATH_TO_USER_HOME)/.vimrc $(PATH_TO_USER_HOME)/.vimrc.bak; \
	fi
	ln -srf vimrc $(PATH_TO_USER_HOME)/.vimrc

.PHONY: remove-check
remove-check:
	rm $(PATH_TO_USER_HOME)/.vimrc


.PHONY: help
help:
	@echo 'Please make sure the user listed below is correct'
	@echo 'User: $(USER)'
	@echo ''
	@echo 'PLEASE READ THE README.md before running any commands'
	@echo 'Usage: make [command]'
	@echo 'install - Install configs using hard symlinks'
	@echo 'remove-check - Remove .vimrc'
