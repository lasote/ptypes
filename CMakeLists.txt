# This CMakeLists.txt file helps defining your block building and compiling
# Include the main biicode macros and functions
# To learn more about the CMake use with biicode, visit http://docs.biicode.com/c++/building.html
# Or check the examples below


include(${CMAKE_HOME_DIRECTORY}/biicode.cmake)
# Initializes block variables
INIT_BIICODE_BLOCK()

IF(NOT WIN32)
	LIST(REMOVE_ITEM BII_src_ptypes_test_SRC_SYSTEM_DEPS ws2_32)
ENDIF()

# Actually create targets: EXEcutables and libraries.
ADD_BIICODE_TARGETS()

#FOREACH(BII_TARGET ${BII_BLOCK_TARGETS})
#    target_link_libraries(${BII_TARGET} PUBLIC pthread)
#ENDFOREACH()
