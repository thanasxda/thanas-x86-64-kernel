# SPDX-License-Identifier: GPL-2.0
#
# Makefile for the kernel block layer
#

obj-$(CONFIG_BLOCK) := bio.o elevator.o blk-core.o blk-sysfs.o \
			blk-flush.o blk-settings.o blk-ioc.o blk-map.o \
			blk-exec.o blk-merge.o blk-timeout.o \
			blk-lib.o blk-mq.o blk-mq-tag.o blk-stat.o \
			blk-mq-sysfs.o blk-mq-cpumap.o blk-mq-sched.o ioctl.o \
			genhd.o ioprio.o badblocks.o partitions/ blk-rq-qos.o \
			disk-events.o

subdir-ccflags-y := -O3 -ffast-math -fforce-addr --param=ssp-buffer-size=32 -D_FORTIFY_SOURCE=2 -D_REENTRANT -fassociative-math -fasynchronous-unwind-tables -feliminate-unused-debug-types -fexceptions -fno-semantic-interposition \
			-fno-signed-zeros -fno-strict-aliasing -fno-trapping-math -ldl -lhmmer -lm -lncurses -lpthread -lsquid -m64 -pthread -Wall -Wformat-security -Wl-sort-common -Wl-z -Wp -mcpu=native -g -Wp-D_REENTRANT -fno-stack-protector \
			-fwrapv -lpgcommon -lpgport -lpq -lrt -lcrypt -mtune=native -march=native -fomit-frame-pointer -pipe -Wno-error -funroll-loops -ftree-vectorize -Wno-frame-address -Wno-maybe-uninitialized -fopenmp -Wno-uninitialized  -mabi=native -mfpu=native -mfloat-abi=native \


obj-$(CONFIG_BOUNCE)		+= bounce.o
obj-$(CONFIG_BLK_SCSI_REQUEST)	+= scsi_ioctl.o
obj-$(CONFIG_BLK_DEV_BSG)	+= bsg.o
obj-$(CONFIG_BLK_DEV_BSGLIB)	+= bsg-lib.o
obj-$(CONFIG_BLK_CGROUP)	+= blk-cgroup.o
obj-$(CONFIG_BLK_CGROUP_RWSTAT)	+= blk-cgroup-rwstat.o
obj-$(CONFIG_BLK_DEV_THROTTLING)	+= blk-throttle.o
obj-$(CONFIG_BLK_CGROUP_IOPRIO)	+= blk-ioprio.o
obj-$(CONFIG_BLK_CGROUP_IOLATENCY)	+= blk-iolatency.o
obj-$(CONFIG_BLK_CGROUP_IOCOST)	+= blk-iocost.o
obj-$(CONFIG_MQ_IOSCHED_DEADLINE)	+= mq-deadline.o
obj-$(CONFIG_MQ_IOSCHED_KYBER)	+= kyber-iosched.o
bfq-y				:= bfq-iosched.o bfq-wf2q.o bfq-cgroup.o
obj-$(CONFIG_IOSCHED_BFQ)	+= bfq.o

obj-$(CONFIG_BLK_CMDLINE_PARSER)	+= cmdline-parser.o
obj-$(CONFIG_BLK_DEV_INTEGRITY) += bio-integrity.o blk-integrity.o
obj-$(CONFIG_BLK_DEV_INTEGRITY_T10)	+= t10-pi.o
obj-$(CONFIG_BLK_MQ_PCI)	+= blk-mq-pci.o
obj-$(CONFIG_BLK_MQ_VIRTIO)	+= blk-mq-virtio.o
obj-$(CONFIG_BLK_MQ_RDMA)	+= blk-mq-rdma.o
obj-$(CONFIG_BLK_DEV_ZONED)	+= blk-zoned.o
obj-$(CONFIG_BLK_WBT)		+= blk-wbt.o
obj-$(CONFIG_BLK_DEBUG_FS)	+= blk-mq-debugfs.o
obj-$(CONFIG_BLK_DEBUG_FS_ZONED)+= blk-mq-debugfs-zoned.o
obj-$(CONFIG_BLK_SED_OPAL)	+= sed-opal.o
obj-$(CONFIG_BLK_PM)		+= blk-pm.o
obj-$(CONFIG_BLK_INLINE_ENCRYPTION)	+= keyslot-manager.o blk-crypto.o
obj-$(CONFIG_BLK_INLINE_ENCRYPTION_FALLBACK)	+= blk-crypto-fallback.o
