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
	cp LICENSE $(DESTDIR)$(PREFIX)/share/doc/$(PROJECT)
## -- BLOCK:license --
## -- BLOCK:man --
install: install-man
install-man:
	mkdir -p $(DESTDIR)$(PREFIX)/share/man/man1
	cp ./gettext-h-i18n.1 $(DESTDIR)$(PREFIX)/share/man/man1
## -- BLOCK:man --
## -- BLOCK:sh --
install: install-sh
install-sh:
	mkdir -p $(DESTDIR)$(PREFIX)/bin
	cp bin/extract-messages_go $(DESTDIR)$(PREFIX)/bin
	cp bin/genl10n_go       $(DESTDIR)$(PREFIX)/bin
	cp bin/gettext-h-i18n--toc $(DESTDIR)$(PREFIX)/bin
	cp bin/gettext-h-i18n   $(DESTDIR)$(PREFIX)/bin
	cp bin/extract-messages_html $(DESTDIR)$(PREFIX)/bin
	cp bin/geni18n_go       $(DESTDIR)$(PREFIX)/bin
## -- BLOCK:sh --
