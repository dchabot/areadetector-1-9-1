TOP=../../..
include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE
#=============================

# This directory contains header files to support libtiff and libjpeg on WIN32.
# These files were obtained from the distribution at
# http://gnuwin32.sourceforge.net/packages/tiff.htm
# http://gnuwin32.sourceforge.net/packages/jpeg.htm
#
# These files for Windows in this directory are needed when GraphicsMagick is not being used.  
# If GraphicsMagick is being used then it comes with its own TIFF and JPEG support and 
# the files in this directory are not used.
INC_cygwin32 += tiff.h tiffio.h tiffvers.h tiffconf.h 
INC_cygwin32 += jpeglib.h jconfig.h jmorecfg.h jerror.h 
# Use these lines to install local versions of these libraries
# Comment them out to use system versions of the libraries
INC_Linux    += tiff.h tiffio.h tiffvers.h tiffconf.h tiffconf-32.h tiffconf-64.h 
INC_Linux    += jpeglib.h jconfig.h jmorecfg.h jerror.h 
INC_solaris  += jconfig.h jerror.h jmorecfg.h jpeglib.h szlib.h zconf.h zlib.h
INC_Darwin   += tiff.h tiffio.h tiffvers.h tiffconf.h
INC_Darwin   += jpeglib.h jconfig.h jmorecfg.h jerror.h

LIB_INSTALLS_solaris += ../os/solaris-sparc/libjpeg.a ../os/solaris-sparc/libsz.a ../os/solaris-sparc/libz.a
LIB_INSTALLS_cygwin32 += ../os/cygwin32/libtiff.lib    ../os/cygwin32/libjpeg.lib    ../os/cygwin32/libz.lib

ifeq (linux-x86_64, $(findstring linux-x86_64, $(T_A)))
LIB_INSTALLS_Linux += ../os/linux-x86_64/libtiff.a ../os/linux-x86_64/libjpeg.a ../os/linux-x86_64/libz.a
else ifeq (linux-x86, $(findstring linux-x86, $(T_A)))
LIB_INSTALLS_Linux += ../os/linux-x86/libtiff.a    ../os/linux-x86/libjpeg.a    ../os/linux-x86/libz.a
else ifeq (darwin-x86, $(findstring darwin-x86, $(T_A)))
LIB_INSTALLS_Darwin += ../os/darwin-x86/libtiff.a ../os/darwin-x86/libjpeg.a
else ifeq (win32-x86, $(findstring win32-x86, $(T_A)))
#LIB_INSTALLS_WIN32 += ../os/win32-x86/libtiff.lib ../os/win32-x86/libjpeg.lib
#BIN_INSTALLS_WIN32 += ../os/win32-x86/libtiff3.dll ../os/win32-x86/jpeg62.dll ../os/win32-x86/zlib1.dll
endif 

#=============================

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE

