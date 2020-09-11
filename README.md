# C Logger: Logger file for C Projects

## Description
This project is taken from @malensek with his permission to share it with the Open Source Community.
Unfortunately C doesn't have a native Logger Library and print statements sometimes don't give me the 
information I want, like the line number or the function I the program is on. 

This header file allows you to painlessly log information right to the Command Line as your program 
executes.


## How to use
    1. logger.h is easy to use. Simply include it in your *.c file and you are off to the races. `#include "logger.h"`

    1. logger.h has two functions you can use, `LOG` and `LOGP`.

    1. LOG:
        11. LOG prints a formatted log message.
        11. Example Usage:
            `LOG("Hello %s, your lucky number is %d\n", "World", 42);`
    1. LOGP:
        11. LOGP prints and unformatted log message (single string).
        11. Example Usage:
            `LOGP("Hello World!");`
    1. How to add to Makefile:
        11. If you are working with a Makefile and are wondering how you can add 
            looger.h to your Makefile here is an example Makefile.
        `
            PROGS = lab02

            all : $(PROGS)

            lab02 : scanner.c logger.h
                gcc -g -o $@ scanner.c

            clean:
                rm -rf $(PROGS) *~
        `

## Want to Contribute?
If you want to add C Logger please make a pull request with the label "improvement"
If you find a bug in C Logger please make an issue with the label "bug"
