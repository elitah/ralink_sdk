EXEC = flash
OBJS = flash_mtd.o
#OBJS = flash.o flash_api.o
#CFLAGS += -I$(ROOTDIR)/$(LINUXDIR)/drivers/flash 

all: $(EXEC) 

$(EXEC): $(OBJS)
	$(CC) $(CFLAGS) $(LDFLAGS) -o $@ $(OBJS)

romfs:
	$(ROMFSINST) /bin/$(EXEC)
	$(ROMFSINST) -e CONFIG_RALINK_RT6855A /sbin/eth_mac.sh

clean:
	-rm -f $(EXEC) *.elf *.gdb *.o

