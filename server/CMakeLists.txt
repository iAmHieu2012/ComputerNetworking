# CMakeList.txt : CMake project for proj1, include source and define
# project specific logic here.
#
include_directories(include)
file(GLOB SOURCES "src/*.cpp")


# Add source to this project's executable.
add_executable(server ${SOURCES})

# TODO: Add tests and install targets if needed.
