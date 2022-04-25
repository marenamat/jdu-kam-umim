FILES := index.html bootstrap.min.css bootstrap.bundle.js style.css static/cesta-lesem.jpg static/logo-web.png 
FILES += static/michel-catalisano-OZDmI-vO7Io-unsplash.jpg static/andrew-ebrahim-zRwXf6PizEo-unsplash.jpg
FILES += static/alex-kondratiev-H9t723yPjYI-unsplash.jpg
FILES += static/yomex-owo-gRTzhQsiVG0-unsplash.jpg
FILES += static/kenny-eliason--Cmz06-0btw-unsplash.jpg

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
