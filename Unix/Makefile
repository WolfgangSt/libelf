ifeq ($(origin SOLUTION_DIR), undefined)
	SOLUTION_DIR := $(shell pwd)/
endif
PROJECT_DIR_LIBELF:=$(dir $(lastword $(MAKEFILE_LIST)))

$(PROJECT_DIR_LIBELF)/../config.h:
	cd $(PROJECT_DIR_LIBELF)/.. && ./configure

clean::
	rm -f $(PROJECT_DIR_LIBELF)/../config.h
	rm -f libelf.so*
	rm -f libelf

libelf : $(PROJECT_DIR_LIBELF)/../config.h
	cd $(PROJECT_DIR_LIBELF)/.. && make
	cp $(PROJECT_DIR_LIBELF)/../lib/libelf.so* .
	cd $(PROJECT_DIR_LIBELF)/.. && make -i clean
	touch libelf


