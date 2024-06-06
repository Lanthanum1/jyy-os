logisim: logisim.c
	gcc -o logisim -I. logisim.c # `-I.`表示包含当前目录下的头文件。

run: logisim
	./logisim | python3 seg-display.py  # The UNIX Philosophy

clean:
	rm -f logisim

.PHONY: run clean
