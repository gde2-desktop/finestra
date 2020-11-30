@INTLTOOL_DESKTOP_RULE@

icondir=$(pkgdatadir)/icons
icon_DATA=finestra-window-demo.png

AM_CPPFLAGS=@FINESTRA_WINDOW_DEMO_CFLAGS@ @FINESTRA_MESSAGE_CFLAGS@ \
	-DFINESTRA_ICON_DIR=\"$(pkgdatadir)/icons\" \
	-DFINESTRA_LOCALEDIR=\"$(prefix)/@DATADIRNAME@/locale\"

finestra_message_SOURCES= 				\
	finestra-message.c

finestra_window_demo_SOURCES=				\
	finestra-window-demo.c

finestra_mag_SOURCES=					\
	finestra-mag.c

finestra_grayscale_SOURCES=				\
	finestra-grayscale.c

bin_PROGRAMS=finestra-message finestra-window-demo

## cheesy hacks I use, don't really have any business existing. ;-)
noinst_PROGRAMS=finestra-mag finestra-grayscale

finestra_message_LDADD= @FINESTRA_MESSAGE_LIBS@
finestra_window_demo_LDADD= @FINESTRA_WINDOW_DEMO_LIBS@
finestra_mag_LDADD= @FINESTRA_WINDOW_DEMO_LIBS@ -lm
finestra_grayscale_LDADD = @FINESTRA_WINDOW_DEMO_LIBS@

EXTRA_DIST=$(icon_DATA)

