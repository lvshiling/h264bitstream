AUTOMAKE_OPTIONS = subdir-objects
ACLOCAL_AMFLAGS = -I m4

AM_CFLAGS = -I. -Wall $(EXTRA_CFLAGS)
AM_LDFLAGS = -lm

bin_PROGRAMS = h264_analyze

lib_LTLIBRARIES = libh264bitstream.la

libh264bitstream_la_LDFLAGS = -no-undefined
libh264bitstream_la_SOURCES = h264_stream.cpp h264_sei.cpp h264_avcc.cpp

h264_analyze_SOURCES = h264_analyze.cpp
h264_analyze_LDADD = libh264bitstream.la

include_HEADERS = h264_stream.h h264_sei.h h264_avcc.h bs.h

clean-local:
	rm -rf *.pc

pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = libh264bitstream.pc
