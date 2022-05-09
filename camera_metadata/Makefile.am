# Build libcamera_metadata.so
lib_LTLIBRARIES = libcamera_metadata.la

libcamera_metadata_la_SOURCES := src/camera_metadata.c
libcamera_metadata_la_SOURCES += src/CameraParameters.cpp
libcamera_metadata_la_SOURCES += src/CameraMetadata.cpp
libcamera_metadata_la_SOURCES += src/VendorTagDescriptor.cpp

libcamera_metadata_la_CFLAGS := -I$(top_srcdir)/include
libcamera_metadata_la_CFLAGS += -I$(top_srcdir)/include/camera
libcamera_metadata_la_CFLAGS += -I$(top_srcdir)/include/system
libcamera_metadata_la_CFLAGS += -std=c99 -lstdc -lpthread -lrt -lm -lglib-2.0

libcamera_metadata_la_CPPFLAGS := -I$(top_srcdir)/include
libcamera_metadata_la_CPPFLAGS += -I$(top_srcdir)/include/camera
libcamera_metadata_la_CPPFLAGS += -I$(top_srcdir)/include/system
libcamera_metadata_la_CPPFLAGS += -std=c++14 -lstdc++ -lpthread -lrt -lm -lglib-2.0
libcamera_metadata_la_LDFLAGS  := -lutils -lbinder

# Export headers
camera_metadata_includedir=$(includedir)/camera
camera_metadata_include_HEADERS := include/camera/camera_metadata_hidden.h
camera_metadata_include_HEADERS += include/camera/CameraParameters.h
camera_metadata_include_HEADERS += include/camera/CameraMetadata.h
camera_metadata_include_HEADERS += include/camera/VendorTagDescriptor.h

camera_metadata_system_includedir=$(includedir)/system
camera_metadata_system_include_HEADERS := include/system/camera_metadata.h
camera_metadata_system_include_HEADERS += include/system/camera_metadata_tags.h
camera_metadata_system_include_HEADERS += include/system/camera_vendor_tags.h

pkgconfigdir   = $(libdir)/pkgconfig
pkgconfig_DATA = libcamera_metadata.pc
EXTRA_DIST     = $(pkgconfig_DATA)
