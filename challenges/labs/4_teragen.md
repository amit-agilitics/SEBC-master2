

Teragen Output with command and time
===========================

```
[centos@ip-172-31-0-59 ~]$ su berkeley
Password:
su: Authentication failure
[centos@ip-172-31-0-59 ~]$ su berkeley
Password:
[berkeley@ip-172-31-0-59 centos]$ time hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-examples.jar teragen -Dmapred.map.tasks=12 -Ddfs.block.size=536870912  65536000 /user/berkeley/tgen
```
##### Your block size was supposed to be 64 MB, according to the instructions. The task container size was supposed to be 512 MiB
```
17/03/24 19:08:45 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-0-59.ap-southeast-1.compute.internal/172.31.0.59:8032
17/03/24 19:08:45 INFO terasort.TeraGen: Generating 65536000 using 12
17/03/24 19:08:45 INFO mapreduce.JobSubmitter: number of splits:12
17/03/24 19:08:45 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
17/03/24 19:08:45 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
17/03/24 19:08:45 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1490381318636_0001
17/03/24 19:08:46 INFO impl.YarnClientImpl: Submitted application application_1490381318636_0001
17/03/24 19:08:46 INFO mapreduce.Job: The url to track the job: http://ip-172-31-0-59.ap-southeast-1.compute.internal:8088/proxy/application_1490381318636_0001/
17/03/24 19:08:46 INFO mapreduce.Job: Running job: job_1490381318636_0001
17/03/24 19:08:53 INFO mapreduce.Job: Job job_1490381318636_0001 running in uber mode : false
17/03/24 19:08:53 INFO mapreduce.Job:  map 0% reduce 0%
17/03/24 19:09:10 INFO mapreduce.Job:  map 6% reduce 0%
17/03/24 19:09:13 INFO mapreduce.Job:  map 25% reduce 0%
17/03/24 19:09:14 INFO mapreduce.Job:  map 27% reduce 0%
17/03/24 19:09:15 INFO mapreduce.Job:  map 32% reduce 0%
17/03/24 19:09:16 INFO mapreduce.Job:  map 33% reduce 0%
17/03/24 19:09:19 INFO mapreduce.Job:  map 39% reduce 0%
17/03/24 19:09:20 INFO mapreduce.Job:  map 40% reduce 0%
17/03/24 19:09:21 INFO mapreduce.Job:  map 42% reduce 0%
17/03/24 19:09:22 INFO mapreduce.Job:  map 43% reduce 0%
17/03/24 19:09:25 INFO mapreduce.Job:  map 47% reduce 0%
17/03/24 19:09:26 INFO mapreduce.Job:  map 48% reduce 0%
17/03/24 19:09:27 INFO mapreduce.Job:  map 50% reduce 0%
17/03/24 19:09:28 INFO mapreduce.Job:  map 51% reduce 0%
17/03/24 19:09:31 INFO mapreduce.Job:  map 55% reduce 0%
17/03/24 19:09:33 INFO mapreduce.Job:  map 57% reduce 0%
17/03/24 19:09:34 INFO mapreduce.Job:  map 59% reduce 0%
17/03/24 19:09:37 INFO mapreduce.Job:  map 62% reduce 0%
17/03/24 19:09:38 INFO mapreduce.Job:  map 63% reduce 0%
17/03/24 19:09:39 INFO mapreduce.Job:  map 64% reduce 0%
17/03/24 19:09:40 INFO mapreduce.Job:  map 67% reduce 0%
17/03/24 19:09:44 INFO mapreduce.Job:  map 70% reduce 0%
17/03/24 19:09:45 INFO mapreduce.Job:  map 71% reduce 0%
17/03/24 19:09:46 INFO mapreduce.Job:  map 72% reduce 0%
17/03/24 19:09:47 INFO mapreduce.Job:  map 74% reduce 0%
17/03/24 19:09:49 INFO mapreduce.Job:  map 75% reduce 0%
17/03/24 19:09:50 INFO mapreduce.Job:  map 78% reduce 0%
17/03/24 19:09:51 INFO mapreduce.Job:  map 79% reduce 0%
17/03/24 19:09:52 INFO mapreduce.Job:  map 80% reduce 0%
17/03/24 19:09:53 INFO mapreduce.Job:  map 82% reduce 0%
17/03/24 19:09:55 INFO mapreduce.Job:  map 83% reduce 0%
17/03/24 19:09:56 INFO mapreduce.Job:  map 85% reduce 0%
17/03/24 19:09:57 INFO mapreduce.Job:  map 86% reduce 0%
17/03/24 19:09:58 INFO mapreduce.Job:  map 87% reduce 0%
17/03/24 19:09:59 INFO mapreduce.Job:  map 89% reduce 0%
17/03/24 19:10:01 INFO mapreduce.Job:  map 90% reduce 0%
17/03/24 19:10:02 INFO mapreduce.Job:  map 93% reduce 0%
17/03/24 19:10:03 INFO mapreduce.Job:  map 94% reduce 0%
17/03/24 19:10:04 INFO mapreduce.Job:  map 96% reduce 0%
17/03/24 19:10:05 INFO mapreduce.Job:  map 97% reduce 0%
17/03/24 19:10:06 INFO mapreduce.Job:  map 99% reduce 0%
17/03/24 19:10:07 INFO mapreduce.Job:  map 100% reduce 0%
17/03/24 19:10:07 INFO mapreduce.Job: Job job_1490381318636_0001 completed successfully
17/03/24 19:10:07 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=1497854
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=1025
		HDFS: Number of bytes written=6553600000
		HDFS: Number of read operations=48
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=24
	Job Counters
		Launched map tasks=12
		Other local map tasks=12
		Total time spent by all maps in occupied slots (ms)=767968
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=767968
		Total vcore-seconds taken by all map tasks=767968
		Total megabyte-seconds taken by all map tasks=786399232
	Map-Reduce Framework
		Map input records=65536000
		Map output records=65536000
		Input split bytes=1025
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=3181
		CPU time spent (ms)=139070
		Physical memory (bytes) snapshot=4623208448
		Virtual memory (bytes) snapshot=33471188992
		Total committed heap usage (bytes)=4236247040
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=140750829423462787
	File Input Format Counters
		Bytes Read=0
	File Output Format Counters
		Bytes Written=6553600000

real	1m24.454s
user	0m7.946s
sys	0m0.345s
```

Tersort Output with command and time
======================================

```
[berkeley@ip-172-31-0-59 centos]$ time hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-examples.jar terasort  /user/berkeley/tgen /user/berkeley/sortedoutput
17/03/24 19:11:20 INFO terasort.TeraSort: starting
17/03/24 19:11:22 INFO input.FileInputFormat: Total input paths to process : 12
Spent 130ms computing base-splits.
Spent 2ms computing TeraScheduler splits.
Computing input splits took 133ms
Sampling 10 splits of 12
Making 8 from 100000 sampled records
Computing parititions took 673ms
Spent 808ms computing partitions.
17/03/24 19:11:22 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-0-59.ap-southeast-1.compute.internal/172.31.0.59:8032
17/03/24 19:11:23 INFO mapreduce.JobSubmitter: number of splits:12
17/03/24 19:11:23 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1490381318636_0002
17/03/24 19:11:24 INFO impl.YarnClientImpl: Submitted application application_1490381318636_0002
17/03/24 19:11:24 INFO mapreduce.Job: The url to track the job: http://ip-172-31-0-59.ap-southeast-1.compute.internal:8088/proxy/application_1490381318636_0002/
17/03/24 19:11:24 INFO mapreduce.Job: Running job: job_1490381318636_0002
17/03/24 19:11:30 INFO mapreduce.Job: Job job_1490381318636_0002 running in uber mode : false
17/03/24 19:11:30 INFO mapreduce.Job:  map 0% reduce 0%
17/03/24 19:11:47 INFO mapreduce.Job:  map 8% reduce 0%
17/03/24 19:11:48 INFO mapreduce.Job:  map 25% reduce 0%
17/03/24 19:11:49 INFO mapreduce.Job:  map 29% reduce 0%
17/03/24 19:11:50 INFO mapreduce.Job:  map 41% reduce 0%
17/03/24 19:11:52 INFO mapreduce.Job:  map 43% reduce 0%
17/03/24 19:11:53 INFO mapreduce.Job:  map 46% reduce 0%
17/03/24 19:11:54 INFO mapreduce.Job:  map 51% reduce 0%
17/03/24 19:11:55 INFO mapreduce.Job:  map 52% reduce 0%
17/03/24 19:11:56 INFO mapreduce.Job:  map 59% reduce 0%
17/03/24 19:11:57 INFO mapreduce.Job:  map 62% reduce 0%
17/03/24 19:11:58 INFO mapreduce.Job:  map 67% reduce 0%
17/03/24 19:12:00 INFO mapreduce.Job:  map 70% reduce 0%
17/03/24 19:12:01 INFO mapreduce.Job:  map 71% reduce 0%
17/03/24 19:12:02 INFO mapreduce.Job:  map 75% reduce 0%
17/03/24 19:12:04 INFO mapreduce.Job:  map 80% reduce 0%
17/03/24 19:12:05 INFO mapreduce.Job:  map 84% reduce 0%
17/03/24 19:12:06 INFO mapreduce.Job:  map 89% reduce 0%
17/03/24 19:12:08 INFO mapreduce.Job:  map 91% reduce 0%
17/03/24 19:12:13 INFO mapreduce.Job:  map 93% reduce 0%
17/03/24 19:12:14 INFO mapreduce.Job:  map 97% reduce 0%
17/03/24 19:12:16 INFO mapreduce.Job:  map 100% reduce 0%
17/03/24 19:12:33 INFO mapreduce.Job:  map 100% reduce 38%
17/03/24 19:12:34 INFO mapreduce.Job:  map 100% reduce 42%
17/03/24 19:12:37 INFO mapreduce.Job:  map 100% reduce 48%
17/03/24 19:12:38 INFO mapreduce.Job:  map 100% reduce 57%
17/03/24 19:12:39 INFO mapreduce.Job:  map 100% reduce 63%
17/03/24 19:12:40 INFO mapreduce.Job:  map 100% reduce 67%
17/03/24 19:12:44 INFO mapreduce.Job:  map 100% reduce 79%
17/03/24 19:12:45 INFO mapreduce.Job:  map 100% reduce 82%
17/03/24 19:12:46 INFO mapreduce.Job:  map 100% reduce 84%
17/03/24 19:12:47 INFO mapreduce.Job:  map 100% reduce 85%
17/03/24 19:12:50 INFO mapreduce.Job:  map 100% reduce 89%
17/03/24 19:12:51 INFO mapreduce.Job:  map 100% reduce 91%
17/03/24 19:12:52 INFO mapreduce.Job:  map 100% reduce 92%
17/03/24 19:12:56 INFO mapreduce.Job:  map 100% reduce 95%
17/03/24 19:12:58 INFO mapreduce.Job:  map 100% reduce 97%
17/03/24 19:13:02 INFO mapreduce.Job:  map 100% reduce 99%
17/03/24 19:13:06 INFO mapreduce.Job:  map 100% reduce 100%
17/03/24 19:13:06 INFO mapreduce.Job: Job job_1490381318636_0002 completed successfully
17/03/24 19:13:06 INFO mapreduce.Job: Counters: 49
	File System Counters
		FILE: Number of bytes read=5792296208
		FILE: Number of bytes written=8669288048
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=6553601860
		HDFS: Number of bytes written=6553600000
		HDFS: Number of read operations=60
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=16
	Job Counters
		Launched map tasks=12
		Launched reduce tasks=8
		Data-local map tasks=12
		Total time spent by all maps in occupied slots (ms)=422441
		Total time spent by all reduces in occupied slots (ms)=314184
		Total time spent by all map tasks (ms)=422441
		Total time spent by all reduce tasks (ms)=314184
		Total vcore-seconds taken by all map tasks=422441
		Total vcore-seconds taken by all reduce tasks=314184
		Total megabyte-seconds taken by all map tasks=432579584
		Total megabyte-seconds taken by all reduce tasks=321724416
	Map-Reduce Framework
		Map input records=65536000
		Map output records=65536000
		Map output bytes=6684672000
		Map output materialized bytes=2887049343
		Input split bytes=1860
		Combine input records=0
		Combine output records=0
		Reduce input groups=65536000
		Reduce shuffle bytes=2887049343
		Reduce input records=65536000
		Reduce output records=65536000
		Spilled Records=196608000
		Shuffled Maps =96
		Failed Shuffles=0
		Merged Map outputs=96
		GC time elapsed (ms)=8862
		CPU time spent (ms)=614710
		Physical memory (bytes) snapshot=12830543872
		Virtual memory (bytes) snapshot=56085082112
		Total committed heap usage (bytes)=11720458240
	Shuffle Errors
		BAD_ID=0
		CONNECTION=0
		IO_ERROR=0
		WRONG_LENGTH=0
		WRONG_MAP=0
		WRONG_REDUCE=0
	File Input Format Counters
		Bytes Read=6553600000
	File Output Format Counters
		Bytes Written=6553600000
17/03/24 19:13:06 INFO terasort.TeraSort: done

real	1m46.491s
user	0m9.834s
sys	0m0.350s
````````````````

The command and output of hdfs dfs -ls /user/berkeley/tgen
===========================================================

```
[berkeley@ip-172-31-0-59 centos]$ hdfs dfs -ls /user/berkeley/tgen
Found 13 items
-rw-r--r--   3 berkeley supergroup          0 2017-03-24 19:10 /user/berkeley/tgen/_SUCCESS
-rw-r--r--   3 berkeley supergroup  546133400 2017-03-24 19:10 /user/berkeley/tgen/part-m-00000
-rw-r--r--   3 berkeley supergroup  546133300 2017-03-24 19:10 /user/berkeley/tgen/part-m-00001
-rw-r--r--   3 berkeley supergroup  546133300 2017-03-24 19:10 /user/berkeley/tgen/part-m-00002
-rw-r--r--   3 berkeley supergroup  546133400 2017-03-24 19:10 /user/berkeley/tgen/part-m-00003
-rw-r--r--   3 berkeley supergroup  546133300 2017-03-24 19:09 /user/berkeley/tgen/part-m-00004
-rw-r--r--   3 berkeley supergroup  546133300 2017-03-24 19:09 /user/berkeley/tgen/part-m-00005
-rw-r--r--   3 berkeley supergroup  546133400 2017-03-24 19:10 /user/berkeley/tgen/part-m-00006
-rw-r--r--   3 berkeley supergroup  546133300 2017-03-24 19:09 /user/berkeley/tgen/part-m-00007
-rw-r--r--   3 berkeley supergroup  546133300 2017-03-24 19:09 /user/berkeley/tgen/part-m-00008
-rw-r--r--   3 berkeley supergroup  546133400 2017-03-24 19:09 /user/berkeley/tgen/part-m-00009
-rw-r--r--   3 berkeley supergroup  546133300 2017-03-24 19:10 /user/berkeley/tgen/part-m-00010
-rw-r--r--   3 berkeley supergroup  546133300 2017-03-24 19:10 /user/berkeley/tgen/part-m-00011
[berkeley@ip-172-31-0-59 centos]$
```

The command and output to show how many blocks are stored under this directory
================================================================================
`````
[berkeley@ip-172-31-0-59 centos]$ hdfs  fsck /user/berkeley/tgen
Connecting to namenode via http://ip-172-31-0-59.ap-southeast-1.compute.internal:50070
FSCK started by berkeley (auth:SIMPLE) from /172.31.0.59 for path /user/berkeley/tgen at Fri Mar 24 19:15:30 UTC 2017
.............Status: HEALTHY
 Total size:	6553600000 B
 Total dirs:	1
 Total files:	13
 Total symlinks:		0
 Total blocks (validated):	24 (avg. block size 273066666 B)
 ```
#### Your average block size is ~270 MiB, despite the setting you gave. This kind of thing is worth noticing as a sanity check. It could have made you wonder why it was so far off from what you specified. I am thinking 24 blocks for ~6 GB of data should have made you wonder.
 ```
 Minimally replicated blocks:	24 (100.0 %)
 Over-replicated blocks:	0 (0.0 %)
 Under-replicated blocks:	0 (0.0 %)
 Mis-replicated blocks:		0 (0.0 %)
 Default replication factor:	3
 Average block replication:	3.0
 Corrupt blocks:		0
 Missing replicas:		0 (0.0 %)
 Number of data-nodes:		4
 Number of racks:		1
FSCK ended at Fri Mar 24 19:15:30 UTC 2017 in 4 milliseconds


The filesystem under path '/user/berkeley/tgen' is HEALTHY
[berkeley@ip-172-31-0-59 centos]$
````

