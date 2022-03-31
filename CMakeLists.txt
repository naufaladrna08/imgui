include_directories(${CMAKE_SOURCE_DIR}/vendors)
include_directories(${CMAKE_SOURCE_DIR}/vendors/glad)
include_directories(${CMAKE_SOURCE_DIR}/vendors/glfw)
include_directories(${CMAKE_SOURCE_DIR}/vendors/imgui)

add_library(imgui SHARED 
  imgui_demo.cpp
  imgui_draw.cpp
  imgui_tables.cpp 
  imgui_widgets.cpp 
  imgui.cpp
  imgui_impl_glfw.cpp
  imgui_impl_opengl3.cpp
)

target_link_libraries(imgui -lGL -lX11 -lpthread -lXrandr -lXi -ldl)