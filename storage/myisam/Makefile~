#--------------------------------------------------------------#
TOP=../../
OUTPUT?=../../output
include $(OUTPUT)/rules.mk
#--------------------------------------------------------------#

#CONFIG_H_FILE:=../include/linux_mysql_config.h

LIBNAME:=libmyisam
LIBLDFLAGS := -Wl,--version-script -Wl,symbol_export -lpthread -lrt
LIBVERSION:=1.0
LIBVERSION_SUB:=5
STATICLIB:= Y
EXTRACFLAGS += -DHAVE_CONFIG_H -I../../regex -I../../sql -I. -I../../include

CPPFLAGS +=  -fno-implicit-templates -fno-exceptions -fno-rtti
#CPPFLAGS:=  -fno-implicit-templates -fno-exceptions

LIBSRCS := mi_open.c mi_extra.c mi_info.c mi_rkey.c \
			mi_rnext.c mi_rnext_same.c \
			mi_search.c mi_page.c mi_key.c mi_locking.c \
			mi_rrnd.c mi_scan.c mi_cache.c \
			mi_statrec.c mi_packrec.c mi_dynrec.c \
			mi_update.c mi_write.c mi_unique.c \
			mi_delete.c \
			mi_rprev.c mi_rfirst.c mi_rlast.c mi_rsame.c \
			mi_rsamepos.c mi_panic.c mi_close.c mi_create.c\
			mi_range.c mi_dbug.c mi_checksum.c mi_log.c \
			mi_changed.c mi_static.c mi_delete_all.c \
			mi_delete_table.c mi_rename.c  mi_check.c \
			mi_keycache.c mi_preload.c \
			ft_parser.c ft_stopwords.c ft_static.c \
			ft_update.c ft_boolean_search.c ft_nlq_search.c sort.c \
			ha_myisam.cpp \
			rt_index.c rt_key.c rt_mbr.c rt_split.c sp_key.c

all: $(LIBNAME)

clean: rules_clean

install: all rules_install

#--------------------------------------------------------------#
include $(OUTPUT)/rules.mk
#--------------------------------------------------------------#

