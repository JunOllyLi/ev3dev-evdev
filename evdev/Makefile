MICROPYTHON_DIR = ../../so-mpy

CFLAGS = -I$(MICROPYTHON_DIR) -I$(MICROPYTHON_DIR)/py
CFLAGS += -I$(MICROPYTHON_DIR)/ports/unix -I$(MICROPYTHON_DIR)/ports/unix/build -DMICROPY_PY_THREAD=0 
CFLAGS += -shared -fPIC

SRC_C = \
	_input.c \

SOLIBS = $(SRC_C:.c=.so)

%.so: %.c
	$(CC) $(CFLAGS) $< -o $@

all: $(SOLIBS)