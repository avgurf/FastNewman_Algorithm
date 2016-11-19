all: fast_newman

CPP_FILES := $(wildcard *.cpp)
OBJ_FILES := $(addprefix bin/,$(notdir $(CPP_FILES:.cpp=.o)))
LD_FLAGS := 
CC_FLAGS :=  -std=c99

fast_newman: $(OBJ_FILES)
	g++  $(LD_FLAGS) -o $@ $^

bin/%.o: %.cpp
	g++ $(CC_FLAGS) -c -o $@ $<

#Clean the build directory
clean: 
	rm -f bin/*