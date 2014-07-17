#--------------------------------------------------------------#
TOP=../
OUTPUT?=../output
include $(OUTPUT)/rules.mk
#--------------------------------------------------------------#

#CONFIG_H_FILE:=../include/linux_mysql_config.h

LIBNAME:=libmystrings
LIBLDFLAGS := -Wl,--version-script -Wl,symbol_export -lpthread -lrt
LIBVERSION:=1.0
LIBVERSION_SUB:=5
STATICLIB:= Y
EXTRACFLAGS:= -DHAVE_CONFIG_H -I. -I../include


LIBSRCS := strxmov.c bmove_upp.c strappend.c strcont.c strend.c strfill.c strcend.c is_prefix.c strstr.c strinstr.c strmake.c strnmov.c strmov.c longlong2str.c bfill.c bmove.c bmove512.c bchange.c strxnmov.c int2str.c str2int.c r_strinstr.c strtod.c strtol.c strtoul.c strtoll.c strtoull.c llstr.c strnlen.c ctype.c ctype-simple.c ctype-mb.c ctype-big5.c ctype-cp932.c ctype-czech.c ctype-eucjpms.c ctype-euc_kr.c ctype-gb2312.c ctype-gbk.c ctype-sjis.c ctype-tis620.c ctype-ujis.c ctype-utf8.c ctype-ucs2.c ctype-uca.c ctype-win1250ch.c ctype-bin.c ctype-latin1.c my_vsnprintf.c xml.c decimal.c ctype-extra.c my_strtoll10.c str_alloc.c my_strchr.c

all: $(LIBNAME)

clean: rules_clean

install: all rules_install

#--------------------------------------------------------------#
include $(OUTPUT)/rules.mk
#--------------------------------------------------------------#

