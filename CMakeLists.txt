cmake_minimum_required(VERSION 3.31)
project(cm 
  VERSION     1.0.0
  LANGUAGES   CXX
)

find_package(wxWidgets COMPONENTS core base xml)
include(${wxWidgets_USE_FILE})

add_Executable(cm src/main.cxx)
target_link_libraries(cm
  PRIVATE
    ${wxWidgets_LIBRARIES}
)
