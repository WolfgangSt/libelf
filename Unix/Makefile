PROJECT=$(shell pwd)

../config.h:
	cd .. && ./configure

clean:
	rm ../config.h
	rm libelf.so*

test: ../config.h
	cd .. && make
	cp ../lib/libelf.so* .
	cd .. && make clean

