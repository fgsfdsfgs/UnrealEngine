project(SoftDrv CXX)

set(SRC_FILES
  "Src/DrawPoly.cpp"
  "Src/DrawSurf.cpp"
  "Src/DrawTile.cpp"
  "Src/Hit.cpp"
  "Src/Line2D.cpp"
  "Src/SoftDrv.cpp"
)

add_library(${PROJECT_NAME} SHARED ${SRC_FILES})

target_include_directories(${PROJECT_NAME}
  PUBLIC
  ${CMAKE_CURRENT_SOURCE_DIR}/Inc
  PRIVATE
  ${CMAKE_CURRENT_SOURCE_DIR}/Src
)

target_link_libraries(${PROJECT_NAME} Render Engine Core)

target_compile_definitions(${PROJECT_NAME} PRIVATE SOFTDRV_EXPORTS)
