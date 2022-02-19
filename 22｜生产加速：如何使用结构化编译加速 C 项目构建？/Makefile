# 用于控制编译细节的自定义宏；
CC = gcc
CFLAGS = -I./include
LDFLAGS = -lm
TARGET_FILE = bin/main

# 描述各个目标的详细编译步骤；
$(TARGET_FILE): $(patsubst src/%.c,src/%.o,$(wildcard src/*.c))
	$(CC) $^ $(LDFLAGS) -o $@

src/%.o: src/%.c include/%.h
	$(CC) $< $(CFLAGS) -c -o $@