# set cmake minimal version
cmake_minimum_required(VERSION 3.30)

# define global standards
set(CMAKE_C_STANDARD 17)
set(CMAKE_C_STANDARD_REQUIRED ON)
set(CMAKE_C_EXTENSIONS OFF)

project(SupplyViewer
    VERSION 0.1.0
    LANGUAGES C
)

# set global options
#option(ENABLE_CLANG_FORMAT ON)

# set cmake module path
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} ${CMAKE_SOURCE_DIR}/cmake/)

# include necessary modules
include(Warnings)


# add main target
set(APPLICATION_NAME SupplyViewer)
add_executable(${APPLICATION_NAME} ${CMAKE_SOURCE_DIR}/main.c)

# link main target

# main target options
target_set_warnings(${APPLICATION_NAME} ON ON)
