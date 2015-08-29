project(game.libretro.lutro)

cmake_minimum_required(VERSION 2.6)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

enable_language(CXX)

find_package(kodi REQUIRED)
find_package(lutro REQUIRED)

set(DEPLIBS lutro)
set(LUTRO_CUSTOM_BINARY ${LUTRO_LIB}
                        game.libretro.lutro${CMAKE_SHARED_LIBRARY_SUFFIX} lutro)

build_addon(game.libretro.lutro LUTRO DEPLIBS)
