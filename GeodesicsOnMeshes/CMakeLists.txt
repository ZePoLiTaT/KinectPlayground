cmake_minimum_required(VERSION 2.8)
if(COMMAND cmake_policy)
cmake_policy(SET CMP0003 NEW)
endif(COMMAND cmake_policy)

PROJECT( Geodesics )

IF(NOT LIBRARY_OUTPUT_PATH)
  SET(LIBRARY_OUTPUT_PATH ${PROJECT_BINARY_DIR}/bin CACHE INTERNAL
    "Single output directory for building all libraries.")
ENDIF(NOT LIBRARY_OUTPUT_PATH)

IF(NOT EXECUTABLE_OUTPUT_PATH)
  SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/bin CACHE INTERNAL
    "Single output directory for building all executables.")
ENDIF(NOT EXECUTABLE_OUTPUT_PATH)

INCLUDE( CTest )
add_subdirectory( FastMarching )
add_subdirectory( Source )
add_subdirectory( Examples )
add_subdirectory( Testing )

