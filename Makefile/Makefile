.PHONY: all, clean
TARGET = hellomake
CFILES = $(wildcard *.c) 		#CFILES = main.c hello.c
OBJS = $(patsubst %.c, %.o, $(CFILES))	#OBJS = main.o hello.o
CC = gcc
INC_FILES = sum.h
CFLAGS = -I.

all: $(TARGET)

$(TARGET): $(OBJS)
	$(CC) -o $@ $(OBJS)

%.o: %.c $(INC_FILES) 
	$(CC) -c -o $@ $< CFLAGS    
clean:
	rm -R $(TARGET) 
	rm -R $(OBJS)
