FILES := index.html bootstrap.min.css style.css
TARGET := trezor:/home/www/jdukamumim.cz/

all:
	echo

install: Makefile $(FILES)
	rsync -avvz --delete-after $(FILES) $(TARGET)

.PHONY: install all
