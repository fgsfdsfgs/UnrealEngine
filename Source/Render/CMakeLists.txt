project(Render CXX)

set(SRC_FILES
  "Src/UnLight.cpp"
  "Src/UnMeshRn.cpp"
  "Src/UnRandom.cpp"
  "Src/UnRender.cpp"
  "Src/UnSoftLn.cpp"
  "Src/UnSpan.cpp"
  "Src/UnSprite.cpp"
  "Src/UnTest.cpp"
  "Src/Render.cpp"
)

add_library(${PROJECT_NAME} SHARED ${SRC_FILES})

target_include_directories(${PROJECT_NAME}
  PUBLIC
  ${CMAKE_CURRENT_SOURCE_DIR}/Inc
  PRIVATE
  ${CMAKE_CURRENT_SOURCE_DIR}/Src
)

target_link_libraries(${PROJECT_NAME} Engine Core)

target_compile_definitions(${PROJECT_NAME} PRIVATE RENDER_EXPORTS)
