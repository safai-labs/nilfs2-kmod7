
VERSION ?= $(shell uname -r | sed -E -e 's/(-[0-9]+).*\.el7/\1.el7/' -e 's/\.x86_64//g' -e 's/-[0-9]+-generic/-generic/')
SUBDIRS = nilfs2-$(VERSION)

.PHONY: subdirs $(SUBDIRS)

subdirs: $(SUBDIRS)

clean: RULE = clean
install: RULE = install
uninstall: RULE = uninstall

all clean install uninstall: $(SUBDIRS)

$(SUBDIRS):
	  $(MAKE) -C $@ $(RULE)
