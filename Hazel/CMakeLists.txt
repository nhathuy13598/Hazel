add_library(Hazel SHARED "./src/api.cpp")
target_include_directories(Hazel PUBLIC "./include/")
target_link_libraries(Hazel PRIVATE compiler_flags)