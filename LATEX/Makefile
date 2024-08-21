GXX = g++
CFLAGS = -std=c++11 -Wall -O0 `pkg-config --cflags opencv4` -O0
LDFLAGS = `pkg-config --libs opencv4` -lm 
PROG = AnalyzeLocation
SRCS = $(wildcard *.cpp)
OBJS = $(SRCS:.cpp=.o)

.PHONY:all
all:$(PROG)

.SUFFIXES: .o .cpp
.cpp.o:
	$(CXX) $(CFLAGS) -c $<

$(PROG): $(OBJS)
	$(CXX) -o $@ $^ $(LDFLAGS)


.PHONY: clean
clean:
	rm -rf $(OBJS) $(PROG)