cmake_minimum_required(VERSION 3.23...3.31)

list(APPEND CMAKE_MODULE_PATH "${CMAKE_CURRENT_LIST_DIR}/cmake")
include(misc_target)
include(set_cxx_standard)
include(target_folder)
include(vs_startup_project)

set_cxx_standard(17)

set(PROJECT_NAME "Boost.Url Example" CACHE "STRING" "Default project name for IDEs")
project("${PROJECT_NAME}" CXX)

include(CTest)

add_subdirectory(libs)
add_subdirectory(tools)

vs_startup_project(url-redirect)

if(BUILD_TESTING)
    add_subdirectory(tests)
endif()

misc_target(FILES
    "CMakePresets.json")
misc_group_sources("Docs" FILES
    "ReadMe.md"
    "BotThoughts.md")
misc_group_sources("CMake Scripts" FILES
    "cmake/misc_target.cmake"
    "cmake/set_cxx_standard.cmake"
    "cmake/target_folder.cmake"
    "cmake/vs_startup_project.cmake")
misc_group_sources("Editing" FILES
    ".clang-format"
    ".editorconfig")
misc_group_sources("Git" FILES
    ".gitignore"
    ".gitmodules")
misc_group_sources("GitHub" FILES
    ".github/workflows/cmake.yml")
misc_group_sources("VcPkg" FILES
    "vcpkg.json")

set(repoName boost-url-example)
set(targetsFile ${repoName}-targets)
install(TARGETS redirect url-redirect url-tool
  EXPORT ${targetsFile}
  ARCHIVE DESTINATION ${CMAKE_INSTALL_LIBDIR}
  LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
  RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
  )
install(DIRECTORY libs/redirect/include/ DESTINATION ${CMAKE_INSTALL_INCLUDEDIR})
if(COMMAND xpExternPackage)
  xpExternPackage(REPO_NAME ${repoName} TARGETS_FILE ${targetsFile}
    LIBRARIES redirect EXE url-redirect PVT_DEPS GTest NO_EXPORT
    WEB "https://www.meetup.com/utah-cpp-programmers/events/313994701/"
    UPSTREAM "github.com/LegalizeAdulthood/boost-url-example"
    DESC "Manipulating URLs with Boost URL"
    )
elseif(NOT DEFINED CMAKE_INSTALL_CMAKEDIR)
  set(CMAKE_INSTALL_CMAKEDIR ${CMAKE_INSTALL_DATADIR}/cmake)
endif()
install(EXPORT ${targetsFile} DESTINATION ${CMAKE_INSTALL_CMAKEDIR} NAMESPACE ${repoName}::)
