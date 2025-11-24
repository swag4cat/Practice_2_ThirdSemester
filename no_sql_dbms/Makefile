CXX = g++
CXXFLAGS = -std=c++17 -O2 -I./include -I./parcer -pthread
SRCDIR = src
CLIENT_SOURCES = $(SRCDIR)/db_client.cpp $(SRCDIR)/utils.cpp
SERVER_SOURCES = $(SRCDIR)/db_server.cpp $(SRCDIR)/utils.cpp $(SRCDIR)/query_evaluator.cpp $(SRCDIR)/btree_index.cpp $(SRCDIR)/collection.cpp
CLIENT_TARGET = db_client
SERVER_TARGET = db_server

all: $(CLIENT_TARGET) $(SERVER_TARGET)

$(CLIENT_TARGET): $(CLIENT_SOURCES)
	$(CXX) $(CXXFLAGS) -o $(CLIENT_TARGET) $(CLIENT_SOURCES)

$(SERVER_TARGET): $(SERVER_SOURCES)
	$(CXX) $(CXXFLAGS) -o $(SERVER_TARGET) $(SERVER_SOURCES)

clean:
	rm -f $(CLIENT_TARGET) $(SERVER_TARGET)

.PHONY: clean all test
