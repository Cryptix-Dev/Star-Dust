link_libraries(glfw glew)
if (BUILD_SHARED_LIBS)
    add_definitions(-DGLFW_DLL -DGLEW_DLL)
endif()

include_directories("${GLFW_SOURCE_DIR}/include"
                    "${GLEW_SOURCE_DIR}/include")

set(star_HEADERS "")
set(star_SOURCES Main.cpp)
                    
add_executable(StarDust ${star_SOURCES} ${star_HEADERS})
