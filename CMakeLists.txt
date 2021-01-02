cmake_minimum_required(VERSION 3.19.2)
project(First-CPP-Project)

option(BUILD_TESTS
	"Turn on build for tests" 
	OFF
)

file(GLOB SRC_FILES
	"src/*.cpp"
)

set(INC_FILES_DIR
	include/
)

if (BUILD_TESTS)
	add_subdirectory(test)
endif()

include_directories(
	${INC_FILES_DIR}
)

add_executable(First_CPP_Project
	${SRC_FILES}
)
