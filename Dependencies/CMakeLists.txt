add_subdirectory(imgui)
add_subdirectory(SDL)

##########################################################################
# Turn off/configure various parts of basis_universal.
option(BUILD_SHARED_LIBS "Build Shared Libraries" OFF)
option(BUILD_TESTS "Build test applications" OFF)
option(BASISU_BUILD_TOOL "Build the tool" OFF)
option(BASISU_INSTALL "Installs basis universal" OFF)
option(BASISU_INSTALL_TOOL "Installs the tool" OFF)
option(BASISU_OPENMP "Allows OpenMP support" OFF)

add_subdirectory(basis_universal)

##########################################################################
# Turn off/configure various parts of glm.
option(GLM_TEST_ENABLE "Build unit tests" OFF)
option(GLM_INSTALL_ENABLE "Allow installing of the library" OFF)
option(BUILD_SHARED_LIBS "Build shared library" OFF)
option(BUILD_STATIC_LIBS "Build static library" OFF)

add_subdirectory(glm)

target_compile_definitions(glm 
  INTERFACE 
    GLM_FORCE_CXX14 
    GLM_FORCE_SIZE_T_LENGTH 
    GLM_FORCE_DEPTH_ZERO_TO_ONE 
    GLM_FORCE_CTOR_INIT 
    GLM_ENABLE_EXPERIMENTAL 
    GLM_FORCE_SILENT_WARNINGS
)