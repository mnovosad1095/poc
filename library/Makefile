CXX = gcc
SOURCES = $(wildcard *.c)
OBJS = $(patsubst %.c, obj/%.o, $(SOURCES))
LIB_NAME = libcs.a
SLIB_NAME = libcs.so
BIN_DIR = bin
OBJ_DIR = obj
CXXFLAGS = -O3
LDLAGS = -O3

all: $(BIN_DIR)/$(LIB_NAME) $(BIN_DIR)/$(SLIB_NAME) make_directories

$(BIN_DIR)/$(SLIB_NAME): $(OBJS)

	$(CXX) $(LDLAGS) -shared -Wl,-soname,libcs.so -o $@ $^

$(BIN_DIR)/$(LIB_NAME): $(OBJS)
	ar rcs $(BIN_DIR)/$(LIB_NAME) $^

$(OBJ_DIR)/%.o: %.c
	$(CXX) -c $(CXXFLAGS) $< -fPIC -o $@

make_directories:
	mkdir -p $(OBJ_DIR)
	mkdir -p $(BIN_DIR)

.PHONY : clean
clean:
	rm -rf obj bin