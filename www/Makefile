FILES := index.html bootstrap.min.css style.css static/cesta-lesem.jpg static/logo-web.png
TARGET := trezor:/home/www/vimkamjdu.cz/
BUILD := build

$(BUILD)/%: %
	mkdir -p $(dir $@)
	cp $< $@

all: $(addprefix $(BUILD)/,$(FILES))

install: Makefile all
	rsync -avvz --delete-after $(BUILD)/ $(TARGET)

clean:
	rm -rf $(BUILD)

.PHONY: install all clean
