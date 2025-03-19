PATH_TO_USER_HOME = /home/$(USER)

# Help Commands
.PHONY: default
default: help

# Main Commands
.PHONY: install
install:
	if [ -d .tmux ]; then \
		ln -sf .tmux $(PATH_TO_USER_HOME)/.tmux
		ln -sf .tmux.conf.local $(PATH_TO_USER_HOME)/.tmux.conf.local
	else
		echo "Please clone down the .tmux submodule"
	fi

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
