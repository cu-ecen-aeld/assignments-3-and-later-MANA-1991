CC_native := gcc
CC_cross := aarch64-none-linux-gnu-gcc

.PHONY: all
all: writer

ifeq ($(CROSS_COMPILE),aarch64-none-linux-gnu-)
  CC := $(CC_cross)
else
  CC := $(CC_native)
endif

writer: writer.o
	$(CC) -o $@ $^

writer.o: writer.c
	$(CC) -c -o $@ $<

.PHONY: clean
clean:
	rm -f writer writer.o
