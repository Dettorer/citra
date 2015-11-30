# Enable modules to include each other's files
include_directories(.)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Werror -Weverything -Wno-padded -Wno-c++98-compat -Wno-c++98-compat-pedantic -Wno-extended-offsetof -Wno-documentation -Wno-exit-time-destructors -Wno-implicit-fallthrough -Wno-global-constructors -Wno-format-nonliteral")

add_subdirectory(common)
add_subdirectory(core)
add_subdirectory(video_core)
if (ENABLE_GLFW)
    add_subdirectory(citra)
endif()
if (ENABLE_QT)
    add_subdirectory(citra_qt)
endif()
