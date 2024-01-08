CXX = cl
CXXFLAGS = /EHsc

CLIENT_TARGET = clientApp
SERVER_TARGET = serverApp

CLIENT_SRCS = main.cpp
CLIENT_OBJS = $(CLIENT_SRCS:.cpp=.obj)

SERVER_SRCS = serverMain.cpp server.cpp PlayingField.cpp
SERVER_OBJS = $(SERVER_SRCS:.cpp=.obj)

DEPS = server.h PlayingField.h

client: $(CLIENT_TARGET)

server: $(SERVER_TARGET)

all: server client

$(CLIENT_TARGET): $(CLIENT_OBJS)
	$(CXX) $(CXXFLAGS) $(CLIENT_OBJS) /Fe$@

$(SERVER_TARGET): $(SERVER_OBJS)
	$(CXX) $(CXXFLAGS) $(SERVER_OBJS) /Fe$@

.cpp.obj:
	$(CXX) $(CXXFLAGS) /c $<

clean:
	del $(CLIENT_OBJS) $(CLIENT_TARGET).exe $(SERVER_OBJS) $(SERVER_TARGET).exe
