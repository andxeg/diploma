CMAKE_MINIMUM_REQUIRED(VERSION 2.8)

PROJECT(prototype)

FILE(GLOB SOURCE_FILES *.cpp)

IF (DL_STRICT) 
   ADD_DEFINITIONS(-DDL_STRICT )
ENDIF(DL_STRICT)

ADD_LIBRARY(${PROJECT_NAME} SHARED ${SOURCE_FILES})
TARGET_LINK_LIBRARIES(${PROJECT_NAME} routing)
