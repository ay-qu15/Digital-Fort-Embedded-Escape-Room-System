# MPLAB IDE generated this makefile for use with GNU make.
# Project: TEST.mcp
# Date: Sat Apr 19 15:08:26 2025

AS = MPASMWIN.exe
CC = 
LD = mplink.exe
AR = mplib.exe
RM = rm

test.cof : test.o
	$(CC) /p16F877A "test.o" /u_DEBUG /z__MPLAB_BUILD=1 /z__MPLAB_DEBUG=1 /o"test.cof" /M"test.map" /W /x

test.o : test.asm ../../../../../Program\ Files\ (x86)/Microchip/MPASM\ Suite/p16f877A.inc
	$(AS) /q /p16F877A "test.asm" /l"test.lst" /e"test.err" /d__DEBUG=1

clean : 
	$(CC) "test.o" "test.hex" "test.err" "test.lst" "test.cof"

