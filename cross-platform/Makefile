VALUE = default

print_value:
	@ echo Value is $(VALUE)

ifeq ($(OS), Windows_NT)
HOME = $(USERPROFILE)
endif

home:
	@ echo There is no place like $(HOME)

LS = docker run \
	--rm -w /app -v "$(realpath .):/app" bash:5 \
	ls

list_all:
	@ $(LS) -la