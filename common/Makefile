# SPDX-License-Identifier: (GPL-2.0)
CC := gcc

all: common_user_bpf_xdp.o common_params.o

CFLAGS := -g -Wall -lbpf

common_params.o: common_params.c common_params.h
	$(CC) $(CFLAGS) -c -o $@ $<

common_user_bpf_xdp.o: common_user_bpf_xdp.c common_user_bpf_xdp.h
	$(CC) $(CFLAGS) -c -o $@ $<

.PHONY: clean

clean:
	rm -f *.o
