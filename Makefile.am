dist_eselectlib_DATA = libs/bin-symlink.bash

EXTRA_DIST = libs/bin-symlink.bash.in

libs/bin-symlink.bash: libs/bin-symlink.bash.in configure.ac
	$(MKDIR_P) libs
	rm -f $@ $@.tmp
	$(SED) -e "s|@VERSION[@]|@VERSION@|" ${srcdir}/$@.in > $@.tmp
	! [ -x $@.in ] || chmod +x $@.tmp
	chmod a-w $@.tmp
	mv $@.tmp $@

EXTRA_DIST += NEWS
NEWS: configure.ac Makefile.am
	git for-each-ref refs/tags --sort '-*committerdate' \
		--format '# %(tag) (%(*committerdate:short))%0a%(contents:body)' \
		> NEWS
