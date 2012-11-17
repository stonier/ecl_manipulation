###############################################################################
# GTest setup
###############################################################################

MACRO(ecl_add_gtest TESTNAME)
  rosbuild_add_gtest(test_${TESTNAME} ${TESTNAME}.cpp)
  target_link_libraries(test_${TESTNAME} ecl_manipulators)
ENDMACRO(ecl_add_gtest)

###############################################################################
# GTests
###############################################################################

ecl_add_gtest(trajectories)
ecl_add_gtest(waypoints)

