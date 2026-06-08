add_library(redirect
    include/redirect/Rewrite.h
    include/redirect/UrlMapper.h
    Rewrite.cpp
    UrlMapper.cpp
)
find_package(Boost REQUIRED COMPONENTS url)
target_include_directories(redirect PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
    $<INSTALL_INTERFACE:${CMAKE_INSTALL_INCLUDEDIR}>
)
target_link_libraries(redirect PUBLIC Boost::url)
target_folder(redirect "Libraries")
