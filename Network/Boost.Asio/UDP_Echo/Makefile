# the compiler: g++ for C++ program, define as g++ for C++
CXX = g++
CC = gcc
RM = rm -f
CFLAGS = $(CXXFLAGS)
# compiler flags:
#  -g    adds debugging information to the executable file
#  -Wall turns on most, but not all, compiler warnings
CXXFLAGS  = -g -Wall -Werror
LDFLAGS = -lboost_system -pthread -lboost_thread
SPECIAL_FLAGS = -std=c++11

# the build target executable:
TARGET = udp_sync_client \
		udp_sync_server \
		udp_async_client \
		udp_async_server

all: $(TARGET)

udp_sync_client: udp_sync_client.cpp
	$(CXX) $(CXXFLAGS) $< -o $@ $(LDFLAGS)

udp_sync_server: udp_sync_server.cpp
	$(CXX) $(CXXFLAGS) $< -o $@ $(LDFLAGS)

udp_async_client: udp_async_client.cpp
	$(CXX) $(CXXFLAGS) $< -o $@ $(LDFLAGS)

udp_async_server: udp_async_server.cpp
	$(CXX) $(CXXFLAGS) $< -o $@ $(LDFLAGS)

clean:
	$(RM) $(TARGET) *.o
