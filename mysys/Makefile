#--------------------------------------------------------------#
TOP=../
OUTPUT?=../output
include $(OUTPUT)/rules.mk
#--------------------------------------------------------------#

#CONFIG_H_FILE:=../include/linux_mysql_config.h
DDEFAULT_BASEDIR:=/usr/local/mysql
MYSQLDATAdir:=/usr/local/mysql/var
#DDEFAULT_CHARSET_HOME=/usr/local/mysql
DSHAREDIR=/usr/local/mysql/share/mysql
DDEFAULT_HOME_ENV=MYSQL_HOME
DDEFAULT_GROUP_SUFFIX_ENV=MYSQL_GROUP_SUFFIX
DDEFAULT_SYSCONFDIR=/usr/local/mysql/etc




LIBNAME:=libmysys
LIBLDFLAGS := -Wl,--version-script -Wl,symbol_export -lpthread -lrt
LIBVERSION:=1.0
LIBVERSION_SUB:=5
STATICLIB:= Y
EXTRACFLAGS +=  -I../zlib -I../include -I.  -DDEFAULT_BASEDIR=\"$(DDEFAULT_BASEDIR)\" \
  				-DMYSQL_DATADIR="\"$(MYSQLDATAdir)\"" \
				-DDEFAULT_CHARSET_HOME="\"$(DDEFAULT_BASEDIR)\"" \
				-DSHAREDIR="\"$(DSHAREDIR)\"" \
				-DDEFAULT_HOME_ENV=$(DDEFAULT_HOME_ENV) \
				-DDEFAULT_GROUP_SUFFIX_ENV=$(DDEFAULT_GROUP_SUFFIX_ENV) \
				-DDEFAULT_SYSCONFDIR="\"$(DDEFAULT_SYSCONFDIR)\"" \
                        	-DHAVE_CONFIG_H

CPPFLAGS +=  -fno-implicit-templates -fno-exceptions -fno-rtti
#CPPFLAGS:=  -fno-implicit-templates -fno-exceptions 


LIBSRCS := my_init.c my_getwd.c mf_getdate.c my_mmap.c mf_path.c mf_loadpath.c my_file.c my_open.c my_create.c my_dup.c my_seek.c my_read.c my_pread.c my_write.c my_getpagesize.c mf_keycaches.c my_crc32.c mf_iocache.c mf_iocache2.c mf_cache.c mf_tempfile.c mf_tempdir.c my_lock.c mf_brkhant.c my_alarm.c my_malloc.c my_realloc.c my_once.c mulalloc.c my_alloc.c safemalloc.c my_new.cpp my_vle.c my_fopen.c my_fstream.c my_getsystime.c my_error.c errors.c my_div.c my_messnc.c mf_format.c mf_same.c mf_dirname.c mf_fn_ext.c my_symlink.c my_symlink2.c mf_pack.c mf_unixpath.c mf_arr_appstr.c mf_wcomp.c mf_wfile.c my_gethwaddr.c mf_qsort.c mf_qsort2.c mf_sort.c ptr_cmp.c mf_radix.c queues.c my_getncpus.c tree.c trie.c list.c hash.c array.c string.c typelib.c my_copy.c my_append.c my_lib.c my_delete.c my_rename.c my_redel.c my_chsize.c my_clock.c my_quick.c my_lockmem.c my_static.c my_sync.c my_getopt.c my_mkdir.c default_modify.c default.c my_compress.c checksum.c my_net.c my_sleep.c charset.c charset-def.c my_bitmap.c my_bit.c md5.c rijndael.c my_aes.c sha1.c my_compare.c my_netware.c my_largepage.c my_memmem.c stacktrace.c my_windac.c my_access.c base64.c my_libwrap.c mf_keycache.c thr_alarm.c thr_lock.c thr_mutex.c thr_rwlock.c my_pthread.c my_thr_init.c mf_keycache.c



all: $(LIBNAME)

clean: rules_clean

install: all rules_install

#--------------------------------------------------------------#
include $(OUTPUT)/rules.mk
#--------------------------------------------------------------#

