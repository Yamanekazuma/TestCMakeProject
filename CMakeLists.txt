cmake_minimum_required (VERSION 3.12)

if (POLICY CMP0141)
  cmake_policy(SET CMP0141 NEW)
  set(CMAKE_MSVC_DEBUG_INFORMATION_FORMAT "$<IF:$<AND:$<C_COMPILER_ID:MSVC>,$<CXX_COMPILER_ID:MSVC>>,$<$<CONFIG:Debug,RelWithDebInfo>:EditAndContinue>,$<$<CONFIG:Debug,RelWithDebInfo>:ProgramDatabase>>")
endif()

project ("TestCMakeProject")
add_executable (TestCMakeProject "TestCMakeProject.c" "TestCMakeProject.h")
set_property(TARGET TestCMakeProject PROPERTY CXX_STANDARD 20)

target_compile_options(TestCMakeProject PRIVATE /W4)
target_link_options(TestCMakeProject PRIVATE /SUBSYSTEM:CONSOLE)
