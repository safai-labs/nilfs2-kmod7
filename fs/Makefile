
SUBDIRS = nilfs2-$(shell uname -r | sed -E -e 's/(-[0-9]+)(\.[0-9]+)+/\1/' -e 's/\.x86_64//g')

.PHONY: subdirs $(SUBDIRS)

subdirs: $(SUBDIRS)

clean: RULE = clean
install: RULE = install
uninstall: RULE = uninstall

all clean install uninstall: $(SUBDIRS)

$(SUBDIRS):
	  $(MAKE) -C $@ $(RULE)
