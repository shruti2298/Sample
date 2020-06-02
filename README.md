lsb_release -a
No LSB modules are available.
Distributor ID:	Ubuntu
Description:	Ubuntu 16.04.6 LTS
Release:	16.04
Codename:	xenial

hostnamectl
   Static hostname: shruti-VirtualBox
         Icon name: computer-vm
           Chassis: vm
        Machine ID: 1fe8c0fa0dbe47378efb2ed6aca99e2d
           Boot ID: 3f0a6f884bed4e3eb92e6d4db1961d1c
    Virtualization: oracle
  Operating System: Ubuntu 16.04.6 LTS
            Kernel: Linux 4.15.0-45-generic
      Architecture: x86-64

cat /etc/*release
DISTRIB_ID=Ubuntu
DISTRIB_RELEASE=16.04
DISTRIB_CODENAME=xenial
DISTRIB_DESCRIPTION="Ubuntu 16.04.6 LTS"
NAME="Ubuntu"
VERSION="16.04.6 LTS (Xenial Xerus)"
ID=ubuntu
ID_LIKE=debian
PRETTY_NAME="Ubuntu 16.04.6 LTS"
VERSION_ID="16.04"
HOME_URL="http://www.ubuntu.com/"
SUPPORT_URL="http://help.ubuntu.com/"
BUG_REPORT_URL="http://bugs.launchpad.net/ubuntu/"
VERSION_CODENAME=xenial
UBUNTU_CODENAME=xenial

java -version
openjdk version "1.8.0_252"
OpenJDK Runtime Environment (build 1.8.0_252-8u252-b09-1~16.04-b09)
OpenJDK 64-Bit Server VM (build 25.252-b09, mixed mode)

mysql -u root -p
Enter password: 
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 3
Server version: 5.7.30-0ubuntu0.16.04.1 (Ubuntu)

Copyright (c) 2000, 2020, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> status
--------------
mysql  Ver 14.14 Distrib 5.7.30, for Linux (x86_64) using  EditLine wrapper

Connection id:		3
Current database:	
Current user:		root@localhost
SSL:			Not in use
Current pager:		stdout
Using outfile:		''
Using delimiter:	;
Server version:		5.7.30-0ubuntu0.16.04.1 (Ubuntu)
Protocol version:	10
Connection:		Localhost via UNIX socket
Server characterset:	latin1
Db     characterset:	latin1
Client characterset:	utf8
Conn.  characterset:	utf8
UNIX socket:		/var/run/mysqld/mysqld.sock
Uptime:			27 min 58 sec

Threads: 1  Questions: 5  Slow queries: 0  Opens: 107  Flush tables: 1  Open tables: 26  Queries per second avg: 0.002

--------------

show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sys                |
+--------------------+
4 rows in set (0,48 sec)

create database Employees;
Query OK, 1 row affected (0,13 sec)

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| Employees          |
| mysql              |
| performance_schema |
| sys                |
+--------------------+
5 rows in set (0,00 sec)

create table info (name varchar(150) NOT NULL, age INT unsigned NOT NULL);
Query OK, 0 rows affected (1,10 sec)

mysql> show tables;
+---------------------+
| Tables_in_Employees |
+---------------------+
| info                |
+---------------------+
1 row in set (0,00 sec)
describe info;
+-------+------------------+------+-----+---------+-------+
| Field | Type             | Null | Key | Default | Extra |
+-------+------------------+------+-----+---------+-------+
| name  | varchar(150)     | NO   |     | NULL    |       |
| age   | int(10) unsigned | NO   |     | NULL    |       |
+-------+------------------+------+-----+---------+-------+

redis-server
6036:C 02 Jun 2020 17:05:25.932 # oO0OoO0OoO0Oo Redis is starting oO0OoO0OoO0Oo
6036:C 02 Jun 2020 17:05:25.932 # Redis version=5.0.8, bits=64, commit=00000000, modified=0, pid=6036, just started
6036:C 02 Jun 2020 17:05:25.932 # Warning: no config file specified, using the default config. In order to specify a config file use redis-server /path/to/redis.conf
6036:M 02 Jun 2020 17:05:25.934 * Increased maximum number of open files to 10032 (it was originally set to 1024).
                _._                                                  
           _.-``__ ''-._                                             
      _.-``    `.  `_.  ''-._           Redis 5.0.8 (00000000/0) 64 bit
  .-`` .-```.  ```\/    _.,_ ''-._                                   
 (    '      ,       .-`  | `,    )     Running in standalone mode
 |`-._`-...-` __...-.``-._|'` _.-'|     Port: 6379
 |    `-._   `._    /     _.-'    |     PID: 6036
  `-._    `-._  `-./  _.-'    _.-'                                   
 |`-._`-._    `-.__.-'    _.-'_.-'|                                  
 |    `-._`-._        _.-'_.-'    |           http://redis.io        
  `-._    `-._`-.__.-'_.-'    _.-'                                   
 |`-._`-._    `-.__.-'    _.-'_.-'|                                  
 |    `-._`-._        _.-'_.-'    |                                  
  `-._    `-._`-.__.-'_.-'    _.-'                                   
      `-._    `-.__.-'    _.-'                                       
          `-._        _.-'                                           
              `-.__.-'                                               

6036:M 02 Jun 2020 17:05:25.947 # WARNING: The TCP backlog setting of 511 cannot be enforced because /proc/sys/net/core/somaxconn is set to the lower value of 128.
6036:M 02 Jun 2020 17:05:25.948 # Server initialized
6036:M 02 Jun 2020 17:05:25.948 # WARNING overcommit_memory is set to 0! Background save may fail under low memory condition. To fix this issue add 'vm.overcommit_memory = 1' to /etc/sysctl.conf and then reboot or run the command 'sysctl vm.overcommit_memory=1' for this to take effect.
6036:M 02 Jun 2020 17:05:25.948 # WARNING you have Transparent Huge Pages (THP) support enabled in your kernel. This will create latency and memory usage issues with Redis. To fix this issue run the command 'echo never > /sys/kernel/mm/transparent_hugepage/enabled' as root, and add it to your /etc/rc.local in order to retain the setting after a reboot. Redis must be restarted after THP is disabled.
6036:M 02 Jun 2020 17:05:25.953 * DB loaded from disk: 0.000 seconds
6036:M 02 Jun 2020 17:05:25.953 * Ready to accept connections

redis-cli
127.0.0.1:6379> info
# Server
redis_version:5.0.8
redis_git_sha1:00000000
redis_git_dirty:0
redis_build_id:129cf1a0751f12a
redis_mode:standalone
os:Linux 4.15.0-45-generic x86_64
arch_bits:64
multiplexing_api:epoll
atomicvar_api:atomic-builtin
gcc_version:5.4.0
process_id:6036
run_id:f3b9adb0652dcd06606199064a7353e0e2cfb424
tcp_port:6379
uptime_in_seconds:31
uptime_in_days:0
hz:10
configured_hz:10
lru_clock:14048452
executable:/home/shruti/redis-server
config_file:

# Clients
connected_clients:1
client_recent_max_input_buffer:2
client_recent_max_output_buffer:0
blocked_clients:0

# Memory
used_memory:855176
used_memory_human:835.13K
used_memory_rss:5533696
used_memory_rss_human:5.28M
used_memory_peak:855176
used_memory_peak_human:835.13K
used_memory_peak_perc:100.12%
used_memory_overhead:841974
used_memory_startup:792280
used_memory_dataset:13202
used_memory_dataset_perc:20.99%
allocator_allocated:1375744
allocator_active:1617920
allocator_resident:8343552
total_system_memory:1033322496
total_system_memory_human:985.45M
used_memory_lua:37888
used_memory_lua_human:37.00K
used_memory_scripts:0
used_memory_scripts_human:0B
number_of_cached_scripts:0
maxmemory:0
maxmemory_human:0B
maxmemory_policy:noeviction
allocator_frag_ratio:1.18
allocator_frag_bytes:242176
allocator_rss_ratio:5.16
allocator_rss_bytes:6725632
rss_overhead_ratio:0.66
rss_overhead_bytes:-2809856
mem_fragmentation_ratio:6.81
mem_fragmentation_bytes:4720520
mem_not_counted_for_evict:0
mem_replication_backlog:0
mem_clients_slaves:0
mem_clients_normal:49694
mem_aof_buffer:0
mem_allocator:jemalloc-5.1.0
active_defrag_running:0
lazyfree_pending_objects:0

# Persistence
loading:0
rdb_changes_since_last_save:0
rdb_bgsave_in_progress:0
rdb_last_save_time:1591106725
rdb_last_bgsave_status:ok
rdb_last_bgsave_time_sec:-1
rdb_current_bgsave_time_sec:-1
rdb_last_cow_size:0
aof_enabled:0
aof_rewrite_in_progress:0
aof_rewrite_scheduled:0
aof_last_rewrite_time_sec:-1
aof_current_rewrite_time_sec:-1
aof_last_bgrewrite_status:ok
aof_last_write_status:ok
aof_last_cow_size:0

# Stats
total_connections_received:1
total_commands_processed:1
instantaneous_ops_per_sec:0
total_net_input_bytes:31
total_net_output_bytes:11468
instantaneous_input_kbps:0.00
instantaneous_output_kbps:0.00
rejected_connections:0
sync_full:0
sync_partial_ok:0
sync_partial_err:0
expired_keys:0
expired_stale_perc:0.00
expired_time_cap_reached_count:0
evicted_keys:0
keyspace_hits:0
keyspace_misses:0
pubsub_channels:0
pubsub_patterns:0
latest_fork_usec:0
migrate_cached_sockets:0
slave_expires_tracked_keys:0
active_defrag_hits:0
active_defrag_misses:0
active_defrag_key_hits:0
active_defrag_key_misses:0

# Replication
role:master
connected_slaves:0
master_replid:26660a4b0c06329aa5f0a93f2dca20b4703a21da
master_replid2:0000000000000000000000000000000000000000
master_repl_offset:0
second_repl_offset:-1
repl_backlog_active:0
repl_backlog_size:1048576
repl_backlog_first_byte_offset:0
repl_backlog_histlen:0

# CPU
used_cpu_sys:0.055000
used_cpu_user:0.033000
used_cpu_sys_children:0.000000
used_cpu_user_children:0.000000

# Cluster
cluster_enabled:0


