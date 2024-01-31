OBJS = input.o job.o main.o

DEPFILES = $(patsubst %.o, %.d, $(OBJS))

INCLUDE_DIR = include

main: $(OBJS)

CC = gcc
CPPFLAGS = -MMD 
CFLAGS = -I$(INCLUDE_DIR) -Werror

-include DEPFILES 

.PHONY: clean
clean:
	rm -f main $(OBJS) $(DEPFILES)
