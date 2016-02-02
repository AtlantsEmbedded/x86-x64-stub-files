Generally, you need to copy these file in an application folder and add a few lines in the makefile such that they get compiled.

Below is an examples of the lines to be added to the Makefile for the wiringPi stub (add them within the blocks that contains similar entries)

(...)

src/wiringPi.c \

(...)

src/wiringPi.o \

(...)

wiringPi.o: src/wiringPi.c 
	$(CC) -c $(CFLAGS) $(INCPATH) -o wiringPi.o src/wiringPi.c

(...)
