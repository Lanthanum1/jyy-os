all: memory stack
TLIB_PATH = ../thread-lib
CFLAGS := -O1 -g -I$(TLIB_PATH)

memory: memory.c
	gcc $(CFLAGS) -o $@ $< -lpthread

stack: stack.c
	gcc $(CFLAGS) -o $@ $< -lpthread

run: all
	@echo ----- Shared Memory Test -----
	@./memory | sort
	@echo ----- Stack Probe Test -----
	@./stack | sort -nk 3  | tail -n 1

clean:
	rm -f memory stack
