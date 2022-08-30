add_library (hello SHARED
  speaker.hpp
  speaker.cpp)

install (TARGETS hello DESTINATION lib)
install (FILES speaker.hpp DESTINATION include)
