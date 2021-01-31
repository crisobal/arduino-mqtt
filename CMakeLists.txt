# Uncompilable CMake File to enable project editing with CLion IDE
cmake_minimum_required(VERSION 3.13)

set(COMPONENT_ADD_INCLUDEDIRS
        src/
        src/lwmqtt
        )


set(COMPONENT_SRCS
        src/lwmqtt/client.c
        src/lwmqtt/helpers.c
        src/lwmqtt/packet.c
        src/lwmqtt/string.c
        src/MQTTClient.cpp)

list(APPEND COMPONENT_REQUIRES "arduino")
register_component()

ADD_DEFINITIONS(-DESP32)

list(APPEND DEFINITIONS "ESP32")

