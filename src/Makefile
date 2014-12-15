CC = gcc
INC_PATH=../include
LIB_PATH=/usr/local/ssl/lib

CFLAGE=-g -I$(INC_PATH)
LIBFLAGE= -L$(LIB_PATH) -lcrypto -L$(LIB_PATH)/engines -lswxa

OBJS=md_engine.o

TAGERT=md_test

all : $(TAGERT)

$(TAGERT) : $(OBJS)
	$(CC) -o $@ $^ $(LIBFLAGE) $(CFLAGE)

%.o:%.c
	$(CC) -c $(CFLAGE) $< -o $@

clean :
	rm *.o $(TAGERT)
