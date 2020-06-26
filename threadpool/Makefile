SRC = ~/build/C-Thread-Pool/thpool.c
OBJ = $(SRC:.c=.o)
OUT = thpool.a
INCLUDES = -I~/build/C-Thread-Pool
CCFLAGS = -g -O2 -fpic
CCC = gcc
LDFLAGS = -g
GIT_SOURCE=https://github.com/Pithikos/C-Thread-Pool.git

.SUFFIXES: .c

all: static

static: $(OUT)

.c.o:
	$(CCC) $(INCLUDES) $(CCFLAGS) $(EXTRACCFLAGS) -c $< -o $@

$(OUT): $(OBJ)
	ar rcs $(OUT) $(OBJ)

clean:
	rm -f $(OBJ) $(OUT) $(DYN)
