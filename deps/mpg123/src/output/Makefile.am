## Makefile.am: produce Makefile.in from this

## copyright by the mpg123 project - free software under the terms of the LGPL 2.1
## see COPYING and AUTHORS files in distribution or http://www.mpg123.org
## initially written by Nicholas J. Humfrey

#AM_CPPFLAGS = -I$(top_srcdir)/src/libmpg123 -I$(top_srcdir)/src
AM_CPPFLAGS = $(LTDLINCL) -I$(top_builddir)/src -I$(top_builddir)/src/libmpg123 -I$(top_srcdir)/src -I$(top_srcdir)/src/libmpg123

#Do not include uneeded headers from mpg123app.h
AM_CPPFLAGS += -DBUILDING_OUTPUT_MODULES=1

if HAVE_MODULES

pkglib_LTLIBRARIES =

# These are not tested and _very_ likely need work: aix alib hp os2 sgi mint

# Use that sh/perl script to generate the module entries:
#for i in alsa coreaudio esd jack nas oss portaudio pulse qsa sdl sndio sun win32 win32_wasapi aix alib arts hp os2 sgi mint openal dummy; do echo $i; done |
#perl -ne 'chomp; $big = uc($_); print <<EOT;
#
#if HAVE_$big
#pkglib_LTLIBRARIES += output_$_.la
#output_${_}_la_SOURCES = $_.c
#output_${_}_la_LDFLAGS = -module -no-undefined -avoid-version -export-dynamic  -export-symbols-regex '"'"'^mpg123_'"'"' \@${big}_LDFLAGS\@
#output_${_}_la_CFLAGS  = \@${big}_CFLAGS\@
#output_${_}_la_LIBADD  = \@${big}_LIBS\@ 
#endif
#EOT
#'

if HAVE_ALSA
pkglib_LTLIBRARIES += output_alsa.la
output_alsa_la_SOURCES = alsa.c
output_alsa_la_LDFLAGS = -module -no-undefined -avoid-version -export-dynamic  -export-symbols-regex '^mpg123_' @ALSA_LDFLAGS@
output_alsa_la_CFLAGS  = @ALSA_CFLAGS@
output_alsa_la_LIBADD  = @ALSA_LIBS@ 
endif

if HAVE_COREAUDIO
pkglib_LTLIBRARIES += output_coreaudio.la
output_coreaudio_la_SOURCES = coreaudio.c
output_coreaudio_la_LDFLAGS = -module -no-undefined -avoid-version -export-dynamic  -export-symbols-regex '^mpg123_' @COREAUDIO_LDFLAGS@
output_coreaudio_la_CFLAGS  = @COREAUDIO_CFLAGS@
output_coreaudio_la_LIBADD  = @COREAUDIO_LIBS@ 
endif

if HAVE_ESD
pkglib_LTLIBRARIES += output_esd.la
output_esd_la_SOURCES = esd.c
output_esd_la_LDFLAGS = -module -no-undefined -avoid-version -export-dynamic  -export-symbols-regex '^mpg123_' @ESD_LDFLAGS@
output_esd_la_CFLAGS  = @ESD_CFLAGS@
output_esd_la_LIBADD  = @ESD_LIBS@ 
endif

if HAVE_JACK
pkglib_LTLIBRARIES += output_jack.la
output_jack_la_SOURCES = jack.c
output_jack_la_LDFLAGS = -module -no-undefined -avoid-version -export-dynamic  -export-symbols-regex '^mpg123_' @JACK_LDFLAGS@
output_jack_la_CFLAGS  = @JACK_CFLAGS@
output_jack_la_LIBADD  = @JACK_LIBS@ 
endif

if HAVE_NAS
pkglib_LTLIBRARIES += output_nas.la
output_nas_la_SOURCES = nas.c
output_nas_la_LDFLAGS = -module -no-undefined -avoid-version -export-dynamic  -export-symbols-regex '^mpg123_' @NAS_LDFLAGS@
output_nas_la_CFLAGS  = @NAS_CFLAGS@
output_nas_la_LIBADD  = @NAS_LIBS@ 
endif

if HAVE_OSS
pkglib_LTLIBRARIES += output_oss.la
output_oss_la_SOURCES = oss.c
output_oss_la_LDFLAGS = -module -no-undefined -avoid-version -export-dynamic  -export-symbols-regex '^mpg123_' @OSS_LDFLAGS@
output_oss_la_CFLAGS  = @OSS_CFLAGS@
output_oss_la_LIBADD  = @OSS_LIBS@ 
endif

if HAVE_PORTAUDIO
pkglib_LTLIBRARIES += output_portaudio.la
output_portaudio_la_SOURCES = portaudio.c
output_portaudio_la_LDFLAGS = -module -no-undefined -avoid-version -export-dynamic  -export-symbols-regex '^mpg123_' @PORTAUDIO_LDFLAGS@
output_portaudio_la_CFLAGS  = @PORTAUDIO_CFLAGS@
output_portaudio_la_LIBADD  = @PORTAUDIO_LIBS@ 
endif

if HAVE_PULSE
pkglib_LTLIBRARIES += output_pulse.la
output_pulse_la_SOURCES = pulse.c
output_pulse_la_LDFLAGS = -module -no-undefined -avoid-version -export-dynamic  -export-symbols-regex '^mpg123_' @PULSE_LDFLAGS@
output_pulse_la_CFLAGS  = @PULSE_CFLAGS@
output_pulse_la_LIBADD  = @PULSE_LIBS@ 
endif

if HAVE_QSA
pkglib_LTLIBRARIES += output_qsa.la
output_qsa_la_SOURCES = qsa.c
output_qsa_la_LDFLAGS = -module -no-undefined -avoid-version -export-dynamic  -export-symbols-regex '^mpg123_' @QSA_LDFLAGS@
output_qsa_la_CFLAGS  = @QSA_CFLAGS@
output_qsa_la_LIBADD  = @QSA_LIBS@ 
endif

if HAVE_SDL
pkglib_LTLIBRARIES += output_sdl.la
output_sdl_la_SOURCES = sdl.c
output_sdl_la_LDFLAGS = -module -no-undefined -avoid-version -export-dynamic  -export-symbols-regex '^mpg123_' @SDL_LDFLAGS@
output_sdl_la_CFLAGS  = @SDL_CFLAGS@
output_sdl_la_LIBADD  = @SDL_LIBS@ 
endif

if HAVE_SNDIO
pkglib_LTLIBRARIES += output_sndio.la
output_sndio_la_SOURCES = sndio.c
output_sndio_la_LDFLAGS = -module -no-undefined -avoid-version -export-dynamic  -export-symbols-regex '^mpg123_' @SNDIO_LDFLAGS@
output_sndio_la_CFLAGS  = @SNDIO_CFLAGS@
output_sndio_la_LIBADD  = @SNDIO_LIBS@ 
endif

if HAVE_SUN
pkglib_LTLIBRARIES += output_sun.la
output_sun_la_SOURCES = sun.c
output_sun_la_LDFLAGS = -module -no-undefined -avoid-version -export-dynamic  -export-symbols-regex '^mpg123_' @SUN_LDFLAGS@
output_sun_la_CFLAGS  = @SUN_CFLAGS@
output_sun_la_LIBADD  = @SUN_LIBS@ 
endif

if HAVE_WIN32
pkglib_LTLIBRARIES += output_win32.la
output_win32_la_SOURCES = win32.c
output_win32_la_LDFLAGS = -module -no-undefined -avoid-version -export-dynamic  -export-symbols-regex '^mpg123_' @WIN32_LDFLAGS@
output_win32_la_CFLAGS  = @WIN32_CFLAGS@
output_win32_la_LIBADD  = @WIN32_LIBS@ 
endif

if HAVE_WIN32_WASAPI
pkglib_LTLIBRARIES += output_win32_wasapi.la
output_win32_wasapi_la_SOURCES = win32_wasapi.c
output_win32_wasapi_la_LDFLAGS = -module -no-undefined -avoid-version -export-dynamic  -export-symbols-regex '^mpg123_' @WIN32_WASAPI_LDFLAGS@
output_win32_wasapi_la_CFLAGS  = @WIN32_WASAPI_CFLAGS@
output_win32_wasapi_la_LIBADD  = @WIN32_WASAPI_LIBS@ 
endif

if HAVE_AIX
pkglib_LTLIBRARIES += output_aix.la
output_aix_la_SOURCES = aix.c
output_aix_la_LDFLAGS = -module -no-undefined -avoid-version -export-dynamic  -export-symbols-regex '^mpg123_' @AIX_LDFLAGS@
output_aix_la_CFLAGS  = @AIX_CFLAGS@
output_aix_la_LIBADD  = @AIX_LIBS@ 
endif

if HAVE_ALIB
pkglib_LTLIBRARIES += output_alib.la
output_alib_la_SOURCES = alib.c
output_alib_la_LDFLAGS = -module -no-undefined -avoid-version -export-dynamic  -export-symbols-regex '^mpg123_' @ALIB_LDFLAGS@
output_alib_la_CFLAGS  = @ALIB_CFLAGS@
output_alib_la_LIBADD  = @ALIB_LIBS@ 
endif

if HAVE_ARTS
pkglib_LTLIBRARIES += output_arts.la
output_arts_la_SOURCES = arts.c
output_arts_la_LDFLAGS = -module -no-undefined -avoid-version -export-dynamic  -export-symbols-regex '^mpg123_' @ARTS_LDFLAGS@
output_arts_la_CFLAGS  = @ARTS_CFLAGS@
output_arts_la_LIBADD  = @ARTS_LIBS@ 
endif

if HAVE_HP
pkglib_LTLIBRARIES += output_hp.la
output_hp_la_SOURCES = hp.c
output_hp_la_LDFLAGS = -module -no-undefined -avoid-version -export-dynamic  -export-symbols-regex '^mpg123_' @HP_LDFLAGS@
output_hp_la_CFLAGS  = @HP_CFLAGS@
output_hp_la_LIBADD  = @HP_LIBS@ 
endif

if HAVE_OS2
pkglib_LTLIBRARIES += output_os2.la
output_os2_la_SOURCES = os2.c
output_os2_la_LDFLAGS = -module -no-undefined -avoid-version -export-dynamic  -export-symbols-regex '^mpg123_' @OS2_LDFLAGS@
output_os2_la_CFLAGS  = @OS2_CFLAGS@
output_os2_la_LIBADD  = @OS2_LIBS@ 
endif

if HAVE_SGI
pkglib_LTLIBRARIES += output_sgi.la
output_sgi_la_SOURCES = sgi.c
output_sgi_la_LDFLAGS = -module -no-undefined -avoid-version -export-dynamic  -export-symbols-regex '^mpg123_' @SGI_LDFLAGS@
output_sgi_la_CFLAGS  = @SGI_CFLAGS@
output_sgi_la_LIBADD  = @SGI_LIBS@ 
endif

if HAVE_MINT
pkglib_LTLIBRARIES += output_mint.la
output_mint_la_SOURCES = mint.c
output_mint_la_LDFLAGS = -module -no-undefined -avoid-version -export-dynamic  -export-symbols-regex '^mpg123_' @MINT_LDFLAGS@
output_mint_la_CFLAGS  = @MINT_CFLAGS@
output_mint_la_LIBADD  = @MINT_LIBS@ 
endif

if HAVE_OPENAL
pkglib_LTLIBRARIES += output_openal.la
output_openal_la_SOURCES = openal.c
output_openal_la_LDFLAGS = -module -no-undefined -avoid-version -export-dynamic  -export-symbols-regex '^mpg123_' @OPENAL_LDFLAGS@
output_openal_la_CFLAGS  = @OPENAL_CFLAGS@
output_openal_la_LIBADD  = @OPENAL_LIBS@ 
endif

if HAVE_DUMMY
pkglib_LTLIBRARIES += output_dummy.la
output_dummy_la_SOURCES = dummy.c
output_dummy_la_LDFLAGS = -module -no-undefined -avoid-version -export-dynamic  -export-symbols-regex '^mpg123_' @DUMMY_LDFLAGS@
output_dummy_la_CFLAGS  = @DUMMY_CFLAGS@
output_dummy_la_LIBADD  = @DUMMY_LIBS@ 
endif

else

# Static build of one module only.

AM_CFLAGS=@OUTPUT_CFLAGS@

all: @OUTPUT_MOD@.$(OBJEXT)

# No installation happening from here
install: all


endif
