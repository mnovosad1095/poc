CXX = gcc
CXXFLAGS = -O3
LDLAGS = -O3
OBJ_DIR = obj
BIN_DIR = bin


all: $(BIN_DIR)/bzip2 $(BIN_DIR)/bzip2recover

$(BIN_DIR)/bzip2: $(OBJ_DIR)/bzip2.o
	$(CXX) $(LDLAGS) $^ -o bin/bzip2 -lcs -L../library/bin

$(BIN_DIR)/bzip2recover: $(OBJ_DIR)/bzip2recover.o
	$(CXX) $(LDLAGS) $^ -o $@ -lcs -L../library/bin

obj/%.o: %.c
	$(CXX) -c $(CXXFLAGS)  $<	-o $@

.PHONY: clean
clean:
	rm -rf obj bin