NAME=sdc-vmtools

ifeq ($(VERSION), "")
	@echo "Use gmake"
endif

# Directories
SRC := $(shell pwd)

# Tools
MAKE = make
TAR = tar
UNAME := $(shell uname)
ifeq ($(UNAME), SunOS)
	MAKE = gmake
	TAR = gtar
	CC = gcc
endif

all:
	bin/build-image

clean:
	@echo "Cleaning"
	rm -fr cache

.PHONY: clean iso tar all
