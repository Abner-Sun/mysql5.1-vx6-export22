#--------------------------------------------------------------#
TOP=../
OUTPUT?=../output
include $(OUTPUT)/rules.mk
#--------------------------------------------------------------#

#CONFIG_H_FILE:=../include/linux_mysql_config.h
#DEFAULT_CHARSET_HOME=/usr/local/mysql
#DEFAULT_BASEDIR:=/usr/local/mysql
# sfh add MYSQLDATAdir:=/usr/local/mysql/var
MYSQLDATAdir:="var/"
# sfh add SHAREDIR=/usr/local/mysql/share/mysql
SHAREDIR="share/mysql/"
# sfh add PLUGINDIR=/usr/local/mysql/lib/mysql/plugin
PLUGINDIR="lib/mysql/plugin"



#lex_hash.h:	gen_lex_hash.cc lex.h
#		$(CCP) -Wl,--allow-shlib-undefined -o gen_lex_hash $(EXEOBJS) $(LDFLAGS) $(EXELDFLAGS)
#		./gen_lex_hash$(EXEEXT) > $@-t
#		$(MV) $@-t $@
#sql_lex.cpp:
#

LIBNAME:=libndb
LIBLDFLAGS := -Wl,--version-script -Wl,symbol_export -lpthread -lrt
LIBVERSION:=1.0
LIBVERSION_SUB:=5
STATICLIB:= Y
EXTRACFLAGS +=  -DMYSQL_SERVER  \
  				-DMYSQL_DATADIR="\"$(MYSQLDATAdir)\"" \
				-DSHAREDIR="\"$(SHAREDIR)\"" \
				-DPLUGINDIR="\"$(PLUGINDIR)\"" \
				-DHAVE_EVENT_SCHEDULER -DHAVE_CONFIG_H \
				-I. -I../include -I../zlib -I../regex -I.

CPPFLAGS +=  -fno-implicit-templates -fno-exceptions -fno-rtti

LIBSRCS := ha_ndbcluster.cpp \
			ha_ndbcluster_binlog.cpp \
			ha_ndbcluster_cond.cpp




EXENAMEP := mysqld

EXELDFLAGS:=    ../lib/libndb.a ../lib/libcsv.a ../lib/libheap.a ../lib/libmyisam.a ../lib/libmyisammrg.a ../lib/libvio.a ../lib/libmysys.a ../lib/libdbug.a ../lib/libregex.a ../lib/libmystrings.a ../lib/libzlt.a

CPPFLAGS +=  -fno-implicit-templates -fno-exceptions -fno-rtti
#CPPFLAGS:=  -fno-implicit-templates -fno-exceptions 

EXESRCS := sql_lex.cpp sql_handler.cpp sql_partition.cpp item.cpp item_sum.cpp item_buff.cpp item_func.cpp item_cmpfunc.cpp item_strfunc.cpp item_timefunc.cpp thr_malloc.cpp item_create.cpp item_subselect.cpp item_row.cpp item_geofunc.cpp item_xmlfunc.cpp field.cpp strfunc.cpp key.cpp sql_class.cpp sql_list.cpp net_serv.cpp protocol.cpp sql_state.c lock.cpp my_lock.c sql_string.cpp sql_manager.cpp sql_map.cpp mysqld.cpp password.c hash_filo.cpp hostname.cpp sql_connect.cpp scheduler.cpp sql_parse.cpp set_var.cpp sql_yacc.cpp sql_base.cpp table.cpp sql_select.cpp sql_insert.cpp sql_profile.cpp sql_prepare.cpp sql_error.cpp sql_locale.cpp sql_update.cpp sql_delete.cpp uniques.cpp sql_do.cpp procedure.cpp sql_test.cpp log.cpp init.cpp derror.cpp sql_acl.cpp unireg.cpp des_key_file.cpp log_event.cpp rpl_record.cpp log_event_old.cpp rpl_record_old.cpp discover.cpp time.cpp opt_range.cpp opt_sum.cpp records.cpp filesort.cpp handler.cpp ha_partition.cpp debug_sync.cpp signal_handler.cpp sql_db.cpp sql_table.cpp sql_rename.cpp sql_crypt.cpp sql_load.cpp mf_iocache.cpp field_conv.cpp sql_show.cpp sql_udf.cpp sql_analyse.cpp sql_cache.cpp slave.cpp sql_repl.cpp rpl_filter.cpp rpl_tblmap.cpp rpl_utility.cpp rpl_injector.cpp rpl_rli.cpp rpl_mi.cpp rpl_reporting.cpp sql_union.cpp sql_derived.cpp sql_client.cpp repl_failsafe.cpp sql_olap.cpp sql_view.cpp gstream.cpp spatial.cpp sql_help.cpp sql_cursor.cpp tztime.cpp my_decimal.cpp sp_head.cpp sp_pcontext.cpp sp_rcontext.cpp sp.cpp sp_cache.cpp parse_file.cpp sql_trigger.cpp event_scheduler.cpp event_data_objects.cpp event_queue.cpp event_db_repository.cpp events.cpp sql_plugin.cpp sql_binlog.cpp sql_builtin.cpp sql_tablespace.cpp partition_info.cpp sql_servers.cpp event_parse_data.cpp mini_client_errors.c pack.c client.c my_time.c my_user.c



all: $(LIBNAME) $(EXENAMEP) 

clean: rules_clean

install: all rules_install

#--------------------------------------------------------------#
include $(OUTPUT)/rules.mk
#--------------------------------------------------------------#

