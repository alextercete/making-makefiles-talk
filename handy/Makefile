VALUE ?= default

print_value:
	@ echo Value is $(VALUE)

release: require_version
	@ echo Starting $(VERSION) release...

require_version:
ifndef VERSION
	$(error You must specify a VERSION variable)
endif

REMOTE_URL = $(shell git remote get-url origin)
ifeq ($(subst git@,,$(REMOTE_URL)), $(REMOTE_URL))
REMOTE_PROTOCOL = HTTPS
else
REMOTE_PROTOCOL = SSH
endif

print_remote_protocol:
	@ echo $(REMOTE_PROTOCOL)