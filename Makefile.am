## Process this file with automake to produce Makefile.in

SUBDIRS = src

EXTRA_DIST = COPYING.3party ChangeLog.LuaAPI FAQ BUGS patches pkgs tests
dist-hook:
	make -C "$(distdir)/tests" clean

# enable generating tags files in particular directories
distcheck-hook:
	mkdir -p $(distdir)/data/vim/doc/app/ $(distdir)/data/vim/doc/plugin/
	chmod u+w $(distdir)/data/vim/doc/app/ $(distdir)/data/vim/doc/plugin/

mostlyclean-local:
	+make -C "$(abs_top_srcdir)/tests" "B=$(abs_builddir)/tests/" clean

force: ;
