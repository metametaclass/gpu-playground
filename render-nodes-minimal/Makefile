TARGET=render-nodes-minimal

all: Makefile $(TARGET)

%.o: %.c
	gcc -c $< -I/usr/include -Wall -Wpedantic -O0 -std=c99 `pkg-config --cflags glesv2 egl gbm` -o $@


$(TARGET): main.o
	gcc $^ -ggdb3 `pkg-config --libs glesv2 egl gbm` -o $@

clean:
	rm -f $(TARGET)
