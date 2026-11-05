CC = gcc
CFLAGS = -Wall -Wextra -O2 -Iinclude -MMD -MP

SRCS = src/main.c src/add.c src/sub.c src/util/stats.c
OBJS = build/main.o build/add.o build/sub.o build/util/stats.o

all: build/prog

build/prog: $(OBJS)
	@mkdir -p build
	$(CC) $(CFLAGS) $^ -o $@

build/%.o: src/%.c
	@mkdir -p $(dir $@)
	$(CC) $(CFLAGS) -c $< -o $@

clean:
	rm -rf build
	
