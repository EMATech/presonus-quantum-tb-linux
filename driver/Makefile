# Out-of-tree ALSA PCI driver for PreSonus Quantum Thunderbolt Family (skeleton)
# Build: make -C /lib/modules/$(uname -r)/build M=$(PWD) modules
# Load:  sudo insmod snd-quantum-tb.ko  (or modprobe after install)

obj-m := snd-quantum-tb.o

KDIR ?= /lib/modules/$(shell uname -r)/build
PWD := $(shell pwd)

all:
	$(MAKE) -C $(KDIR) M=$(PWD) modules

clean:
	$(MAKE) -C $(KDIR) M=$(PWD) clean

install: all
	$(MAKE) -C $(KDIR) M=$(PWD) modules_install
	depmod -a

.PHONY: all clean install
