PROJECT=sh-gettext
VERSION=1.0.0
PREFIX=/usr/local
all:
clean:
install:

## -- BLOCK:license --
install: install-license
install-license: 
	mkdir -p $(DESTDIR)$(PREFIX)/share/doc/$(PROJECT)
	cp LICENSE  $(DESTDIR)$(PREFIX)/share/doc/$(PROJECT)
## -- BLOCK:license --
## -- BLOCK:sh --
install: install-sh
install-sh:
	mkdir -p $(DESTDIR)$(PREFIX)/bin
	cp bin/gettext-h-i18n--go $(DESTDIR)$(PREFIX)/bin
	cp bin/gettext-h-i18n--go-gen $(DESTDIR)$(PREFIX)/bin
	cp bin/gettext-h-i18n--toc $(DESTDIR)$(PREFIX)/bin
	cp bin/gettext-h-i18n   $(DESTDIR)$(PREFIX)/bin
	cp bin/gettext-h-i18n--html $(DESTDIR)$(PREFIX)/bin
## -- BLOCK:sh --
