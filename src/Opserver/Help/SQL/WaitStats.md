﻿SQL Waits
------------------------
Waits are stalls that threads hit when doing work in SQL server. This can range from waiting on disk and network I/O to waiting on memory between NUMA nodes to synchronize.



SQL Server Wait Types
-------------------------
There are many types of waits in SQL Server, the most common ones are explained here:

 - ABR
 - AM_INDBUILD_ALLOCATION
 - AM_SCHEMAMGR_UNSHARED_CACHE
 - ASSEMBLY_LOAD
 - ASYNC_DISKPOOL_LOCK
 - ASYNC_IO_COMPLETION
 - ASYNC_NETWORK_IO
 - ASYNC_OP_COMPLETION
 - ASYNC_OP_CONTEXT_READ
 - ASYNC_OP_CONTEXT_WRITE
 - AUDIT_GROUPCACHE_LOCK
 - AUDIT_LOGINCACHE_LOCK
 - AUDIT_ON_DEMAND_TARGET_LOCK
 - AUDIT_XE_SESSION_MGR
 - BACKUP
 - BACKUP_OPERATOR
 - BACKUPBUFFER
 - BACKUPIO
 - BACKUPTHREAD
 - BAD_PAGE_PROCESS
 - BMPALLOCATION
 - BMPBUILD
 - BMPREPARTITION
 - BMPREPLICATION
 - BROKER_CONNECTION_RECEIVE_TASK
 - BROKER_DISPATCHER
 - BROKER_ENDPOINT_STATE_MUTEX
 - BROKER_EVENTHANDLER
 - BROKER_FORWARDER
 - BROKER_INIT
 - BROKER_MASTERSTART
 - BROKER_RECEIVE_WAITFOR
 - BROKER_REGISTERALLENDPOINTS
 - BROKER_SERVICE
 - BROKER_SHUTDOWN
 - BROKER_TASK_SHUTDOWN
 - BROKER_TASK_STOP
 - BROKER_TASK_SUBMIT
 - BROKER_TO_FLUSH
 - BROKER_TRANSMISSION_OBJECT
 - BROKER_TRANSMISSION_TABLE
 - BROKER_TRANSMISSION_WORK
 - BROKER_TRANSMITTER
 - BUILTIN_HASHKEY_MUTEX
 - CHANGE_TRACKING_WAITFORCHANGES
 - CHECK_PRINT_RECORD
 - CHECKPOINT_QUEUE
 - CHKPT
 - CLEAR_DB
 - CLR_AUTO_EVENT
 - CLR_CRST
 - CLR_JOIN
 - CLR_MANUAL_EVENT
 - CLR_MEMORY_SPY
 - CLR_MONITOR
 - CLR_RWLOCK_READER
 - CLR_RWLOCK_WRITER
 - CLR_SEMAPHORE
 - CLR_TASK_START
 - CLRHOST_STATE_ACCESS
 - CMEMTHREAD
 - COLUMNSTORE_BUILD_THROTTLE
 - COMMIT_TABLE
 - COUNTRECOVERYMGR
 - CREATE_DATINISERVICE
 - CXPACKET
 - CXROWSET_SYNC
 - DAC_INIT
 - DBCC_SCALE_OUT_EXPR_CACHE
 - DBMIRROR_DBM_EVENT
 - DBMIRROR_DBM_MUTEX
 - DBMIRROR_EVENTS_QUEUE
 - DBMIRROR_SEND
 - DBMIRROR_WORKER_QUEUE
 - DBMIRRORING_CMD
 - DBSEEDING_FLOWCONTROL
 - DBSEEDING_OPERATION
 - DBSTATE
 - DEADLOCK_ENUM_MUTEX
 - DEADLOCK_TASK_SEARCH
 - DEBUG
 - DIRTY_PAGE_POLL
 - DIRTY_PAGE_SYNC
 - DISABLE_VERSIONING
 - DISKIO_SUSPEND
 - DISPATCHER_PRIORITY_QUEUE_SEMAPHORE
 - DISPATCHER_QUEUE_SEMAPHORE
 - DLL_LOADING_MUTEX
 - DROP_DATABASE_TIMER_TASK
 - DROPTEMP
 - DTC
 - DTC_ABORT_REQUEST
 - DTC_RESOLVE
 - DTC_STATE
 - DTC_TMDOWN_REQUEST
 - DTC_WAITFOR_OUTCOME
 - DTCPNTSYNC
 - DUMP_LOG_COORDINATOR
 - DUMP_LOG_COORDINATOR_QUEUE
 - DUMPTRIGGER
 - EC
 - EE_PMOLOCK
 - EE_SPECPROC_MAP_INIT
 - ENABLE_EMPTY_VERSIONING
 - ENABLE_VERSIONING
 - ERROR_REPORTING_MANAGER
 - EXCHANGE
 - EXECSYNC
 - EXECUTION_PIPE_EVENT_INTERNAL
 - FABRIC_HADR_TRANSPORT_CONNECTION
 - FABRIC_REPLICA_CONTROLLER_LIST
 - FABRIC_REPLICA_CONTROLLER_STATE_AND_CONFIG
 - FABRIC_REPLICA_PUBLISHER_EVENT_PUBLISH
 - FABRIC_REPLICA_PUBLISHER_SUBSCRIBER_LIST
 - FABRIC_WAIT_FOR_BUILD_REPLICA_EVENT_PROCESSING
 - FAILPOINT
 - FCB_REPLICA_READ
 - FCB_REPLICA_WRITE
 - FEATURE_SWITCHES_UPDATE
 - FFT_NSO_DB_KILL_FLAG
 - FFT_NSO_DB_LIST
 - FFT_NSO_FCB
 - FFT_NSO_FCB_FIND
 - FFT_NSO_FCB_PARENT
 - FFT_NSO_FCB_RELEASE_CACHED_ENTRIES
 - FFT_NSO_FILEOBJECT
 - FFT_NSO_TABLE_LIST
 - FFT_NTFS_STORE
 - FFT_RECOVERY
 - FFT_RSFX_COMM
 - FFT_RSFX_WAIT_FOR_MEMORY
 - FFT_STARTUP_SHUTDOWN
 - FFT_STORE_DB
 - FFT_STORE_ROWSET_LIST
 - FFT_STORE_TABLE
 - FILESTREAM_CACHE
 - FILESTREAM_CHUNKER
 - FILESTREAM_CHUNKER_INIT
 - FILESTREAM_FCB
 - FILESTREAM_FILE_OBJECT
 - FILESTREAM_WORKITEM_QUEUE
 - FILETABLE_SHUTDOWN
 - FS_FC_RWLOCK
 - FS_GARBAGE_COLLECTOR_SHUTDOWN
 - FS_HEADER_RWLOCK
 - FS_LOGTRUNC_RWLOCK
 - FSA_FORCE_OWN_XACT
 - FSAGENT
 - FSTR_CONFIG_MUTEX
 - FSTR_CONFIG_RWLOCK
 - FT_COMPROWSET_RWLOCK
 - FT_IFTS_RWLOCK
 - FT_IFTS_SCHEDULER_IDLE_WAIT
 - FT_IFTSHC_MUTEX
 - FT_IFTSISM_MUTEX
 - FT_MASTER_MERGE
 - FT_MASTER_MERGE_COORDINATOR
 - FT_METADATA_MUTEX
 - FT_PROPERTYLIST_CACHE
 - FT_RESTART_CRAWL
 - FULLTEXT GATHERER
 - GDMA_GET_RESOURCE_OWNER
 - GHOSTCLEANUPSYNCMGR
 - GUARDIAN
 - HADR_AG_MUTEX
 - HADR_AR_CRITICAL_SECTION_ENTRY
 - HADR_AR_MANAGER_MUTEX
 - HADR_AR_UNLOAD_COMPLETED
 - HADR_ARCONTROLLER_NOTIFICATIONS_SUBSCRIBER_LIST
 - HADR_BACKUP_BULK_LOCK
 - HADR_BACKUP_QUEUE
 - HADR_CLUSAPI_CALL
 - HADR_COMPRESSED_CACHE_SYNC
 - HADR_CONNECTIVITY_INFO
 - HADR_DATABASE_FLOW_CONTROL
 - HADR_DATABASE_VERSIONING_STATE
 - HADR_DATABASE_WAIT_FOR_RESTART
 - HADR_DATABASE_WAIT_FOR_TRANSITION_TO_VERSIONING
 - HADR_DB_COMMAND
 - HADR_DB_OP_COMPLETION_SYNC
 - HADR_DB_OP_START_SYNC
 - HADR_DBR_SUBSCRIBER
 - HADR_DBR_SUBSCRIBER_FILTER_LIST
 - HADR_DBSEEDING
 - HADR_DBSEEDING_LIST
 - HADR_DBSTATECHANGE_SYNC
 - HADR_FABRIC_CALLBACK
 - HADR_FILESTREAM_BLOCK_FLUSH
 - HADR_FILESTREAM_FILE_CLOSE
 - HADR_FILESTREAM_FILE_REQUEST
 - HADR_FILESTREAM_IOMGR
 - HADR_FILESTREAM_IOMGR_IOCOMPLETION
 - HADR_FILESTREAM_MANAGER
 - HADR_GROUP_COMMIT
 - HADR_LOGCAPTURE_SYNC
 - HADR_LOGCAPTURE_WAIT
 - HADR_LOGPROGRESS_SYNC
 - HADR_NOTIFICATION_DEQUEUE
 - HADR_NOTIFICATION_WORKER_EXCLUSIVE_ACCESS
 - HADR_NOTIFICATION_WORKER_STARTUP_SYNC
 - HADR_NOTIFICATION_WORKER_TERMINATION_SYNC
 - HADR_PARTNER_SYNC
 - HADR_READ_ALL_NETWORKS
 - HADR_RECOVERY_WAIT_FOR_CONNECTION
 - HADR_RECOVERY_WAIT_FOR_UNDO
 - HADR_REPLICAINFO_SYNC
 - HADR_SYNC_COMMIT
 - HADR_SYNCHRONIZING_THROTTLE
 - HADR_TDS_LISTENER_SYNC
 - HADR_TDS_LISTENER_SYNC_PROCESSING
 - HADR_TIMER_TASK
 - HADR_TRANSPORT_DBRLIST
 - HADR_TRANSPORT_FLOW_CONTROL
 - HADR_TRANSPORT_SESSION
 - HADR_WORK_POOL
 - HADR_WORK_QUEUE
 - HADR_XRF_STACK_ACCESS
 - HTBUILD
 - HTDELETE
 - HTMEMO
 - HTREINIT
 - HTREPARTITION
 - HTTP_ENUMERATION
 - HTTP_START
 - HTTP_STORAGE_CONNECTION
 - IMPPROV_IOWAIT
 - INTERNAL_TESTING
 - IO_AUDIT_MUTEX
 - IO_COMPLETION
 - IO_RETRY
 - IOAFF_RANGE_QUEUE
 - KSOURCE_WAKEUP
 - KTM_ENLISTMENT
 - KTM_RECOVERY_MANAGER
 - KTM_RECOVERY_RESOLUTION
 - LATCH_DT
 - LATCH_EX
 - LATCH_KP
 - LATCH_NL
 - LATCH_SH
 - LATCH_UP
 - LAZYWRITER_SLEEP
 - LCK_M_BU
 - LCK_M_BU_ABORT_BLOCKERS
 - LCK_M_BU_LOW_PRIORITY
 - LCK_M_IS
 - LCK_M_IS_ABORT_BLOCKERS
 - LCK_M_IS_LOW_PRIORITY
 - LCK_M_IU
 - LCK_M_IU_ABORT_BLOCKERS
 - LCK_M_IU_LOW_PRIORITY
 - LCK_M_IX
 - LCK_M_IX_ABORT_BLOCKERS
 - LCK_M_IX_LOW_PRIORITY
 - LCK_M_RIn_NL
 - LCK_M_RIn_NL_ABORT_BLOCKERS
 - LCK_M_RIn_NL_LOW_PRIORITY
 - LCK_M_RIn_S
 - LCK_M_RIn_S_ABORT_BLOCKERS
 - LCK_M_RIn_S_LOW_PRIORITY
 - LCK_M_RIn_U
 - LCK_M_RIn_U_ABORT_BLOCKERS
 - LCK_M_RIn_U_LOW_PRIORITY
 - LCK_M_RIn_X
 - LCK_M_RIn_X_ABORT_BLOCKERS
 - LCK_M_RIn_X_LOW_PRIORITY
 - LCK_M_RS_S
 - LCK_M_RS_S_ABORT_BLOCKERS
 - LCK_M_RS_S_LOW_PRIORITY
 - LCK_M_RS_U
 - LCK_M_RS_U_ABORT_BLOCKERS
 - LCK_M_RS_U_LOW_PRIORITY
 - LCK_M_RX_S
 - LCK_M_RX_S_ABORT_BLOCKERS
 - LCK_M_RX_S_LOW_PRIORITY
 - LCK_M_RX_U
 - LCK_M_RX_U_ABORT_BLOCKERS
 - LCK_M_RX_U_LOW_PRIORITY
 - LCK_M_RX_X
 - LCK_M_RX_X_ABORT_BLOCKERS
 - LCK_M_RX_X_LOW_PRIORITY
 - LCK_M_S
 - LCK_M_S_ABORT_BLOCKERS
 - LCK_M_S_LOW_PRIORITY
 - LCK_M_SCH_M
 - LCK_M_SCH_M_ABORT_BLOCKERS
 - LCK_M_SCH_M_LOW_PRIORITY
 - LCK_M_SCH_S
 - LCK_M_SCH_S_ABORT_BLOCKERS
 - LCK_M_SCH_S_LOW_PRIORITY
 - LCK_M_SIU
 - LCK_M_SIU_ABORT_BLOCKERS
 - LCK_M_SIU_LOW_PRIORITY
 - LCK_M_SIX
 - LCK_M_SIX_ABORT_BLOCKERS
 - LCK_M_SIX_LOW_PRIORITY
 - LCK_M_U
 - LCK_M_U_ABORT_BLOCKERS
 - LCK_M_U_LOW_PRIORITY
 - LCK_M_UIX
 - LCK_M_UIX_ABORT_BLOCKERS
 - LCK_M_UIX_LOW_PRIORITY
 - LCK_M_X
 - LCK_M_X_ABORT_BLOCKERS
 - LCK_M_X_LOW_PRIORITY
 - LOGBUFFER
 - LOGCAPTURE_LOGPOOLTRUNCPOINT
 - LOGGENERATION
 - LOGMGR
 - LOGMGR_FLUSH
 - LOGMGR_QUEUE
 - LOGMGR_RESERVE_APPEND
 - LOGPOOL_CACHESIZE
 - LOGPOOL_CONSUMER
 - LOGPOOL_CONSUMERSET
 - LOGPOOL_FREEPOOLS
 - LOGPOOL_MGRSET
 - LOGPOOL_REPLACEMENTSET
 - LOGPOOLREFCOUNTEDOBJECT_REFDONE
 - LOWFAIL_MEMMGR_QUEUE
 - MD_AGENT_YIELD
 - MD_LAZYCACHE_RWLOCK
 - MISCELLANEOUS
 - MSQL_DQ
 - MSQL_XACT_MGR_MUTEX
 - MSQL_XACT_MUTEX
 - MSQL_XP
 - MSSEARCH
 - NET_WAITFOR_PACKET
 - NODE_CACHE_MUTEX
 - OLEDB
 - ONDEMAND_TASK_QUEUE
 - PAGEIOLATCH_DT
 - PAGEIOLATCH_EX
 - PAGEIOLATCH_KP
 - PAGEIOLATCH_NL
 - PAGEIOLATCH_SH
 - PAGEIOLATCH_UP
 - PAGELATCH_DT
 - PAGELATCH_EX
 - PAGELATCH_KP
 - PAGELATCH_NL
 - PAGELATCH_SH
 - PAGELATCH_UP
 - PARALLEL_BACKUP_QUEUE
 - PERFORMANCE_COUNTERS_RWLOCK
 - PHYSICAL_SEEDING_DMV
 - PREEMPTIVE_*
 - PRINT_ROLLBACK_PROGRESS
 - PRU_ROLLBACK_DEFERRED
 - PWAIT_ALL_COMPONENTS_INITIALIZED
 - PWAIT_COOP_SCAN
 - PWAIT_EVENT_SESSION_INIT_MUTEX
 - PWAIT_HADR_ACTION_COMPLETED
 - PWAIT_HADR_CHANGE_NOTIFIER_TERMINATION_SYNC
 - PWAIT_HADR_CLUSTER_INTEGRATION
 - PWAIT_HADR_FAILOVER_COMPLETED
 - PWAIT_HADR_JOIN
 - PWAIT_HADR_OFFLINE_COMPLETED
 - PWAIT_HADR_ONLINE_COMPLETED
 - PWAIT_HADR_POST_ONLINE_COMPLETED
 - PWAIT_HADR_SERVER_READY_CONNECTIONS
 - PWAIT_HADR_WORKITEM_COMPLETED
 - PWAIT_LOG_CONSOLIDATION_IO
 - PWAIT_LOG_CONSOLIDATION_POLL
 - PWAIT_MD_LOGIN_STATS
 - PWAIT_MD_RELATION_CACHE
 - PWAIT_MD_SERVER_CACHE
 - PWAIT_MD_UPGRADE_CONFIG
 - PWAIT_PREEMPTIVE_AUDIT_ACCESS_WINDOWSLOG
 - PWAIT_QRY_BPMEMORY
 - PWAIT_REPLICA_ONLINE_INIT_MUTEX
 - PWAIT_RESOURCE_SEMAPHORE_FT_PARALLEL_QUERY_SYNC
 - PWAIT_SECURITY_CACHE_INVALIDATION
 - PWAIT_XTP_FSSTORAGE_MAINTENANCE
 - QDS_ASYNC_CHECK_CONSISTENCY_TASK
 - QDS_ASYNC_PERSIST_TASK
 - QDS_ASYNC_PERSIST_TASK_START
 - QDS_BCKG_TASK
 - QDS_CLEANUP_STALE_QUERIES_TASK_MAIN_LOOP_SLEEP
 - QDS_CTXS
 - QDS_DB_DISK
 - QDS_DYN_VECTOR
 - QDS_LOADDB
 - QDS_PERSIST_TASK_MAIN_LOOP_SLEEP
 - QDS_SHUTDOWN_QUEUE
 - QDS_STMT
 - QDS_STMT_DISK
 - QDS_TASK_SHUTDOWN
 - QDS_TASK_START
 - QPJOB_KILL
 - QPJOB_WAITFOR_ABORT
 - QRY_MEM_GRANT_INFO_MUTEX
 - QRY_PARALLEL_THREAD_MUTEX
 - QUERY_EXECUTION_INDEX_SORT_EVENT_OPEN
 - QUERY_NOTIFICATION_MGR_MUTEX
 - QUERY_NOTIFICATION_SUBSCRIPTION_MUTEX
 - QUERY_NOTIFICATION_TABLE_MGR_MUTEX
 - QUERY_NOTIFICATION_UNITTEST_MUTEX
 - QUERY_OPTIMIZER_PRINT_MUTEX
 - QUERY_TASK_ENQUEUE_MUTEX
 - QUERY_TRACEOUT
 - RECOVER_CHANGEDB
 - REDO_THREAD_PENDING_WORK
 - REDO_THREAD_SYNC
 - REPL_CACHE_ACCESS
 - REPL_HISTORYCACHE_ACCESS
 - REPL_SCHEMA_ACCESS
 - REPL_TRANFSINFO_ACCESS
 - REPL_TRANHASHTABLE_ACCESS
 - REPL_TRANTEXTINFO_ACCESS
 - REPLICA_WRITES
 - REQUEST_DISPENSER_PAUSE
 - REQUEST_FOR_DEADLOCK_SEARCH
 - RESMGR_THROTTLED
 - RESOURCE_GOVERNOR_IDLE
 - RESOURCE_QUEUE
 - RESOURCE_SEMAPHORE
 - RESOURCE_SEMAPHORE_MUTEX
 - RESOURCE_SEMAPHORE_QUERY_COMPILE
 - RG_RECONFIG
 - RTDATA_LIST
 - SCAN_CHAR_HASH_ARRAY_INITIALIZATION
 - SEC_DROP_TEMP_KEY
 - SECURITY_CRYPTO_CONTEXT_MUTEX
 - SECURITY_KEYRING_RWLOCK
 - SECURITY_MUTEX
 - SECURITY_RULETABLE_MUTEX
 - SEMPLAT_DSI_BUILD
 - SEQUENCE_GENERATION
 - SEQUENTIAL_GUID
 - SERVER_IDLE_CHECK
 - SERVER_RECONFIGURE
 - SHUTDOWN
 - SLEEP_BPOOL_FLUSH
 - SLEEP_DBSTARTUP
 - SLEEP_DCOMSTARTUP
 - SLEEP_MASTERDBREADY
 - SLEEP_MASTERMDREADY
 - SLEEP_MASTERUPGRADED
 - SLEEP_MSDBSTARTUP
 - SLEEP_SYSTEMTASK
 - SLEEP_TASK
 - SLEEP_TEMPDBSTARTUP
 - SLO_UPDATE
 - SNI_CONN_DUP
 - SNI_CRITICAL_SECTION
 - SNI_HTTP_WAITFOR_0_DISCON
 - SNI_LISTENER_ACCESS
 - SNI_TASK_COMPLETION
 - SOAP_READ
 - SOAP_WRITE
 - SOS_CALLBACK_REMOVAL
 - SOS_DISPATCHER_MUTEX
 - SOS_MEMORY_TOPLEVELBLOCKALLOCATOR
 - SOS_MEMORY_USAGE_ADJUSTMENT
 - SOS_OBJECT_STORE_DESTROY_MUTEX
 - SOS_PHYS_PAGE_CACHE
 - SOS_PROCESS_AFFINITY_MUTEX
 - SOS_SCHEDULER_YIELD
 - SOS_SMALL_PAGE_ALLOC
 - SOS_STACKSTORE_INIT_MUTEX
 - SOS_SYNC_TASK_ENQUEUE_EVENT
 - SOS_VIRTUALMEMORY_LOW
 - SOSHOST_EVENT
 - SOSHOST_INTERNAL
 - SOSHOST_MUTEX
 - SOSHOST_RWLOCK
 - SOSHOST_SEMAPHORE
 - SOSHOST_SLEEP
 - SOSHOST_TRACELOCK
 - SOSHOST_WAITFORDONE
 - SP_PREEMPTIVE_SERVER_DIAGNOSTICS_SLEEP
 - SP_SERVER_DIAGNOSTICS_BUFFER_ACCESS
 - SP_SERVER_DIAGNOSTICS_INIT_MUTEX
 - SP_SERVER_DIAGNOSTICS_SLEEP
 - SQLCLR_APPDOMAIN
 - SQLCLR_ASSEMBLY
 - SQLCLR_DEADLOCK_DETECTION
 - SQLCLR_QUANTUM_PUNISHMENT
 - SQLSORT_NORMMUTEX
 - SQLSORT_SORTMUTEX
 - SQLTRACE_FILE_BUFFER
 - SQLTRACE_FILE_READ_IO_COMPLETION
 - SQLTRACE_FILE_WRITE_IO_COMPLETION
 - SQLTRACE_INCREMENTAL_FLUSH_SLEEP
 - SQLTRACE_PENDING_BUFFER_WRITERS
 - SQLTRACE_SHUTDOWN
 - SQLTRACE_WAIT_ENTRIES
 - SRVPROC_SHUTDOWN
 - STARTUP_DEPENDENCY_MANAGER
 - TEMPOBJ
 - TERMINATE_LISTENER
 - THREADPOOL
 - TIMEPRIV_TIMEPERIOD
 - TRACE_EVTNOTIF
 - TRACEWRITE
 - TRAN_MARKLATCH_DT
 - TRAN_MARKLATCH_EX
 - TRAN_MARKLATCH_KP
 - TRAN_MARKLATCH_NL
 - TRAN_MARKLATCH_SH
 - TRAN_MARKLATCH_UP
 - TRANSACTION_MUTEX
 - UCS_ENDPOINT_CHANGE
 - UCS_MANAGER
 - UCS_MEMORY_NOTIFICATION
 - UCS_SESSION_REGISTRATION
 - UCS_TRANSPORT
 - UCS_TRANSPORT_STREAM_CHANGE
 - UTIL_PAGE_ALLOC
 - VDI_CLIENT_COMPLETECOMMAND
 - VDI_CLIENT_GETCOMMAND
 - VDI_CLIENT_OPERATION
 - VDI_CLIENT_OTHER
 - VERSIONING_COMMITTING
 - VIA_ACCEPT
 - VIEW_DEFINITION_MUTEX
 - WAIT_FOR_RESULTS
 - WAIT_SCRIPTDEPLOYMENT_REQUEST
 - WAIT_SCRIPTDEPLOYMENT_WORKER
 - WAIT_XTP_ASYNC_TX_COMPLETION
 - WAIT_XTP_CKPT_AGENT_WAKEUP
 - WAIT_XTP_CKPT_CLOSE
 - WAIT_XTP_CKPT_ENABLED
 - WAIT_XTP_CKPT_STATE_LOCK
 - WAIT_XTP_GUEST
 - WAIT_XTP_HOST_WAIT
 - WAIT_XTP_OFFLINE_CKPT_BEFORE_REDO
 - WAIT_XTP_OFFLINE_CKPT_LOG_IO
 - WAIT_XTP_OFFLINE_CKPT_NEW_LOG
 - WAIT_XTP_PROCEDURE_ENTRY
 - WAIT_XTP_RECOVERY
 - WAIT_XTP_TASK_SHUTDOWN
 - WAIT_XTP_TRAN_DEPENDENCY
 - WAITFOR
 - WAITFOR_PER_QUEUE
 - WAITFOR_TASKSHUTDOWN
 - WAITSTAT_MUTEX
 - WCC
 - WINFAB_API_CALL
 - WINFAB_REPLICA_BUILD_OPERATION
 - WORKTBL_DROP
 - WRITE_COMPLETION
 - WRITELOG
 - XACT_OWN_TRANSACTION
 - XACT_RECLAIM_SESSION
 - XACTLOCKINFO
 - XACTWORKSPACE_MUTEX
 - XDES_HISTORY
 - XDES_OUT_OF_ORDER_LIST
 - XDES_SNAPSHOT
 - XDESTSVERMGR
 - XE_BUFFERMGR_ALLPROCESSED_EVENT
 - XE_BUFFERMGR_FREEBUF_EVENT
 - XE_CALLBACK_LIST
 - XE_CX_FILE_READ
 - XE_DISPATCHER_CONFIG_SESSION_LIST
 - XE_DISPATCHER_JOIN
 - XE_DISPATCHER_WAIT
 - XE_LIVE_TARGET_TVF
 - XE_MODULEMGR_SYNC
 - XE_OLS_LOCK
 - XE_SERVICES_EVENTMANUAL
 - XE_SERVICES_MUTEX
 - XE_SERVICES_RWLOCK
 - XE_SESSION_CREATE_SYNC
 - XE_SESSION_FLUSH
 - XE_SESSION_SYNC
 - XE_STM_CREATE
 - XE_TIMER_EVENT
 - XE_TIMER_MUTEX
 - XE_TIMER_TASK_DONE
 - XTP_HOST_DB_COLLECTION
 - XTP_HOST_LOG_ACTIVITY
 - XTPPROC_CACHE_ACCESS
 - XTPPROC_PARTITIONED_STACK_CREATE


SQL Server Documentation Links:

 - [sys.dm_os_wait_stats](http://msdn.microsoft.com/en-us/library/ms179984.aspx)