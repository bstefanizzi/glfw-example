
CXX := g++
CXXFLAGS := -Wall -g -I/opt/local/include -I$(HOME)/local/include
LDFLAGS := -L/opt/local/lib -L$(HOME)/local/lib -lopenctm -lglfw -lpng -framework Cocoa -framework OpenGL
TARGET := $(shell basename $(PWD))
OBJECTS := $(patsubst %.cpp,%.o,$(wildcard *.cpp))

%.o: %.cpp
	$(CXX) $(CXXFLAGS) -c $<

all: $(TARGET)

$(TARGET):  $(OBJECTS)
	$(CXX) $(LDFLAGS) $(OBJECTS) -o $@

clean:
	rm -f $(TARGET) $(OBJECTS)

