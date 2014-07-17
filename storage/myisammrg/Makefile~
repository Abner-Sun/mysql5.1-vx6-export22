#--------------------------------------------------------------#
TOP=../../
OUTPUT?=../../output
include $(OUTPUT)/rules.mk
#--------------------------------------------------------------#

#CONFIG_H_FILE:=../include/linux_mysql_config.h

LIBNAME:=libmyisammrg
LIBLDFLAGS := -Wl,--version-script -Wl,symbol_export -lpthread -lrt
LIBVERSION:=1.0
LIBVERSION_SUB:=5
STATICLIB:= Y
EXTRACFLAGS +=  -DHAVE_CONFIG_H -I../../regex -I../../sql -I. -I../../include

CPPFLAGS +=  -fno-implicit-templates -fno-exceptions -fno-rtti
#CPPFLAGS:=  -fno-implicit-templates -fno-exceptions 

LIBSRCS := myrg_open.c myrg_extra.c myrg_info.c myrg_locking.c \
			myrg_rrnd.c myrg_update.c myrg_delete.c myrg_rsame.c \
			myrg_panic.c myrg_close.c myrg_create.c myrg_static.c \
			myrg_rkey.c myrg_rfirst.c myrg_rlast.c myrg_rnext.c \
			myrg_rprev.c myrg_queue.c myrg_write.c myrg_range.c \
			ha_myisammrg.cpp \
			myrg_rnext_same.c myrg_records.c

all: $(LIBNAME)

clean: rules_clean

install: all rules_install

#--------------------------------------------------------------#
include $(OUTPUT)/rules.mk
#--------------------------------------------------------------#

