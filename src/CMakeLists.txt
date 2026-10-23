add_subdirectory(common)
add_subdirectory(util)
add_subdirectory(core)
add_subdirectory(scmversion)
# استبدال واجهة الكمبيوتر Qt بواجهة الـ PS4 XMB
# add_subdirectory(duckstation-qt)
add_subdirectory(duckstation-ps4)

if(APPLE)
  add_subdirectory(updater)
endif()

if(BUILD_REGTEST)
  add_subdirectory(duckstation-regtest)
endif()

if(BUILD_TESTS)
  add_subdirectory(common-tests EXCLUDE_FROM_ALL)
  add_subdirectory(core-tests EXCLUDE_FROM_ALL)
  add_subdirectory(util-tests EXCLUDE_FROM_ALL)
endif()
