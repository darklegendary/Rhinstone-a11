ifdef CONFIG_FUNCTION_TRACER
CFLAGS_REMOVE_clock.o = -pg
endif

CFLAGS_core.o := -fno-omit-frame-pointer

ifdef CONFIG_SCHED_BFS
obj-y += bfs.o clock.o
else
obj-y += core.o clock.o idle_task.o fair.o rt.o stop_task.o
obj-$(CONFIG_SCHED_AUTOGROUP) += auto_group.o
obj-$(CONFIG_SCHED_DEBUG) += debug.o
endif
obj-$(CONFIG_SMP) += cpupri.o
obj-$(CONFIG_SCHEDSTATS) += stats.o


