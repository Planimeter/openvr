set(TARGET_NAME driver_googlevr)

add_library(${TARGET_NAME} SHARED
  driverlog.cpp
  driverlog.h
  driver_googlevr.cpp
)

add_definitions(-DDRIVER_GVR_EXPORTS)

target_link_libraries(${TARGET_NAME}
  ${OPENVR_LIBRARIES}
  ${CMAKE_DL_LIBS}
)

setTargetOutputDirectory(${TARGET_NAME})
