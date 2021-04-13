# locate the necessary dependencies
# FIND_PACKAGE(my_example_library REQUIRED)

# add the necessary include directories
INCLUDE_DIRECTORIES(../include)

# application source files
SET(sources ${PROJECT_NAME}.cpp)

# application header files
SET(headers ../include/${PROJECT_NAME}.h)

# create the executable file
ADD_EXECUTABLE(${PROJECT_NAME} ${sources})


find_package(OpenCV REQUIRED )

# link necessary libraries
TARGET_LINK_LIBRARIES(${PROJECT_NAME} ${OpenCV_LIBS} )

#ADD_DEPENDENCIES(${PROJECT_NAME} my_example_library_target)
