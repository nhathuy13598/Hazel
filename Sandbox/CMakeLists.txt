add_executable(Sandbox "./src/main.cpp")
target_link_libraries(Sandbox PRIVATE compiler_flags)
target_link_libraries(Sandbox PRIVATE spdlog::spdlog spdlog::spdlog_header_only)
target_link_libraries(Sandbox PRIVATE Hazel)

add_custom_command(TARGET Sandbox
  POST_BUILD
  COMMAND ${CMAKE_COMMAND} -E copy $<TARGET_FILE:Hazel> $<TARGET_FILE_DIR:Sandbox>
)