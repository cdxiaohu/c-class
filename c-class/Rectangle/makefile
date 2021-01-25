.PHONY: clean
#all: main.o rect.o shape.o main.i librect.a
all: main.o rect.o shape.o
	gcc main.o src/rect.o src/shape.o -o bin/rect

main.o: main.c include/rect.h include/shape.h
	gcc -I include/ -c main.c

rect.o: src/rect.c include/rect.h include/shape.h
	gcc -I include/ -c src/rect.c -o src/rect.o

shape.o: src/shape.c include/rect.h include/shape.h
	gcc -I include/ -c src/shape.c -o src/shape.o

clean: main.c include/rect.h include/shape.h
	rm src/rect.o src/shape.o main.o bin/rect
