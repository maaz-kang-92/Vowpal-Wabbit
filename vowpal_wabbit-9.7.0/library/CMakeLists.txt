add_executable(library_example library_example.cc)
target_link_libraries(library_example PRIVATE vw_core)
set_target_properties(library_example PROPERTIES FOLDER Examples)

add_executable(test_search test_search.cc)
target_link_libraries(test_search PRIVATE vw_core)
set_target_properties(test_search PROPERTIES FOLDER Examples)

add_executable(search_generate search_generate.cc)
target_link_libraries(search_generate PRIVATE vw_core)
set_target_properties(search_generate PROPERTIES FOLDER Examples)

if(NOT WIN32)
  add_executable(recommend recommend.cc)
  target_link_libraries(recommend PRIVATE vw_core)

  add_executable(gd_mf_weights gd_mf_weights.cc)
  target_link_libraries(gd_mf_weights PRIVATE vw_core)
endif()
