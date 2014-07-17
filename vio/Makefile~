#--------------------------------------------------------------#
TOP=../
OUTPUT?=../output
include $(OUTPUT)/rules.mk
#--------------------------------------------------------------#




LIBNAME:=libvio
LIBLDFLAGS := -Wl,--version-script -Wl,symbol_export -lpthread -lrt
LIBVERSION:=1.0
LIBVERSION_SUB:=5
STATICLIB:= Y
EXTRACFLAGS +=  -DHAVE_CONFIG_H -I.  -I../include

LIBSRCS := vio.c viosocket.c viossl.c viosslfactories.c


all: $(LIBNAME)

clean: rules_clean

install: all rules_install

#--------------------------------------------------------------#
include $(OUTPUT)/rules.mk
#--------------------------------------------------------------#

