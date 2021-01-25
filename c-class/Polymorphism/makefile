.PHONY: clean
#all: main.o main.i circle.o rect.o shape.o libploy.a
all: main.o circle.o rect.o shape.o
	gcc main.o src/circle.o src/rect.o src/shape.o -o bin/ploy

main.o: main.c include/circle.h include/rect.h include/shape.h 
	gcc -I include -c main.c

circle.o: include/circle.h include/shape.h src/circle.c src/shape.c 
	gcc -I include -c src/circle.c -o src/circle.o

rect.o: include/rect.h include/shape.h src/rect.c src/shape.c 
	gcc -I include -c src/rect.c -o src/rect.o

shape.o: include/shape.h src/shape.c 
	gcc -I include -c src/shape.c -o src/shape.o 

clean:
	rm *.o src/*.o bin/*
