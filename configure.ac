AC_PREREQ([2.59])
AC_INIT([eselect-lib-bin-symlink], [0.1.1],
	[https://bitbucket.org/mgorny/eselect-lib-bin-symlink/issues],,
	[https://bitbucket.org/mgorny/eselect-lib-bin-symlink])
AC_CONFIG_AUX_DIR([build-aux])
AM_INIT_AUTOMAKE([1.6 foreign dist-bzip2 no-dependencies])

AC_ARG_WITH([eselectlibdir],
	AS_HELP_STRING([--with-eselectlibdir=DIR], [the eselect libs directory (DATAROOTDIR/eselect/libs)]),
	[], [with_eselectlibdir='${datarootdir}/eselect/libs'])

AC_SUBST([eselectlibdir], [${with_eselectlibdir}])

AC_PROG_MKDIR_P
AC_PROG_SED

AC_CONFIG_FILES([Makefile])
AC_OUTPUT
