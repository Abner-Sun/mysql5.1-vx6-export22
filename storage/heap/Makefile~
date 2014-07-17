#--------------------------------------------------------------#
TOP=../../
OUTPUT?=../../output
include $(OUTPUT)/rules.mk
#--------------------------------------------------------------#

#CONFIG_H_FILE:=../include/linux_mysql_config.h

LIBNAME:=libheap
LIBLDFLAGS := -Wl,--version-script -Wl,symbol_export -lpthread -lrt
LIBVERSION:=1.0
LIBVERSION_SUB:=5
STATICLIB:= Y
EXTRACFLAGS +=  -DHAVE_CONFIG_H -I../../regex -I../../sql -I. -I../../include

CPPFLAGS +=  -fno-implicit-templates -fno-exceptions -fno-rtti
#CPPFLAGS:=  -fno-implicit-templates -fno-exceptions 

LIBSRCS := hp_open.c hp_extra.c hp_close.c hp_panic.c hp_info.c \
			hp_rrnd.c hp_scan.c hp_update.c hp_write.c hp_delete.c \
			hp_rsame.c hp_create.c hp_rename.c hp_rfirst.c \
			hp_rnext.c hp_rlast.c hp_rprev.c hp_clear.c \
			hp_rkey.c hp_block.c \
			ha_heap.cpp \
			hp_hash.c _check.c _rectest.c hp_static.c

all: $(LIBNAME)

clean: rules_clean

install: all rules_install

#--------------------------------------------------------------#
include $(OUTPUT)/rules.mk
#--------------------------------------------------------------#

