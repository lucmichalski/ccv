cmake_minimum_required(VERSION 3.0)

include("cmake/HunterGate.cmake")

include("cmake/HunterGate.cmake")
HunterGate(
    URL "https://github.com/ruslo/hunter/archive/v0.14.25.tar.gz"
    SHA1 "a7ba9775c1206ced7cac204db802b116736ca481"
)

### Import sugar for source collection ###
hunter_add_package(Sugar)
include("${SUGAR_ROOT}/cmake/Sugar")
include(sugar_include)
include(CheckLibraryExists)

project(ccv VERSION 0.7)

include_directories(lib)

add_subdirectory(lib)
option(CCV_BUILD_EXAMPLES OFF)
if(CCV_BUILD_EXAMPLES)
  add_subdirectory(bin)
endif()