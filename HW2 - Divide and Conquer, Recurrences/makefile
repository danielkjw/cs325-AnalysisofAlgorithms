PROJ = Lab3
$(CXX) = g++

SRC  = main.cpp
SRC += space.cpp
SRC += character.cpp
SRC += armory.cpp
SRC += cafeteria.cpp
SRC += command.cpp
SRC += Cyborg.cpp
SRC += Echo1.cpp
SRC += gameEngine.cpp
SRC += hall1.cpp
SRC += Hounds.cpp
SRC += lab.cpp
SRC += library.cpp
SRC += Necromancer.cpp
SRC += prison.cpp
SRC += item.cpp


OBJ = $(SRC:.cpp=.o)


BIN = $(PROJ).bin

CFLAGS = -g -v -Wall -pedantic -std=gnu++11 

VOPT = --tool=memcheck --leak-check=full --show-leak-kinds=all --track-origins=yes --show-reachable=yes


.PHONY: default debug clean zip

default: clean $(BIN) debug


debug: $(BIN)
	@valgrind $(VOPT) ./$(BIN)

$(BIN): $(OBJ)
	@echo "CC	$@"1
	@$(CXX) $(CFLAGS) $^ -o $@

%.o: %.cpp
	@echo "CC	$^"
	@$(CXX) $(CFLAGS) -c $^

clean: $(CLEAN)
	@echo "RM	*.o"
	@echo "RM	$(BIN)"
	@rm -f *.o $(BIN)

