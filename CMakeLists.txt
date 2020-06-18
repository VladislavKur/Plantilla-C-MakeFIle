
project(Prueba)

### PARA AÑADIR CARPETAS Y LIBRERIAS
add_library(libModulos STATIC)
add_subdirectory(ej_modulos)



set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++1y -Wall -Wextra")
add_executable(Prueba main.cpp)

## add_executable (OtroEjecutable otro.cpp)


## PARA APUNTAR LAS LIBRERIAS A LOS EJECUTABLES
target_link_libraries(Prueba libModulos)

set(CMAKE_MODULE_PATH "${CMAKE_CURRENT_LIST_DIR}/cmake_modules")







