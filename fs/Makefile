
SUBDIRS = nilfs2-$(shell uname -r | sed -E 's/(-[0-9]+).*/\1.el7/')

.PHONY: subdirs $(SUBDIRS)

subdirs: $(SUBDIRS)

clean: RULE = clean
install: RULE = install
uninstall: RULE = uninstall

all clean install uninstall: $(SUBDIRS)

$(SUBDIRS):
	  $(MAKE) -C $@ $(RULE)
