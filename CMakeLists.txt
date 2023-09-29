# CMakeLists.txt for ImGui

# Add ImGui as a static library
file(GLOB IMGUI_SOURCE_FILES
    "*.cpp"
    "*.h"
)

message(STATUS "IMGUI DIR: ${CMAKE_CURRENT_SOURCE_DIR}")

add_library(ImGui STATIC ${IMGUI_SOURCE_FILES})

# Include directories for ImGui
target_include_directories(ImGui PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}
)

# Set C++ standard and options
set_target_properties(ImGui PROPERTIES
    CXX_STANDARD 17
    CXX_EXTENSIONS OFF
)

