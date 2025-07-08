# crazyflie-gz-plugins


```
# Harmonic
if("$ENV{GZ_VERSION}" STREQUAL "harmonic")
  find_package(gz-sim8 REQUIRED)
  set(GZ_SIM_VER ${gz-sim8_VERSION_MAJOR})
  message(STATUS "Compiling against Gazebo Harmonic")
  find_package(gz-transport REQUIRED NAMES gz-transport13)
  find_package(gz-msgs REQUIRED NAMES gz-msgs10)
# Default to Garden
else()
  find_package(gz-sim7 REQUIRED)
  set(GZ_SIM_VER ${gz-sim7_VERSION_MAJOR})
  message(STATUS "Compiling against Gazebo Garden")
  find_package(gz-transport REQUIRED NAMES gz-transport12)
  find_package(gz-msgs REQUIRED NAMES gz-msgs9)
endif()
```