project(rtv1 C)
cmake_minimum_required(VERSION 3.9)

add_subdirectory(vendor/libft)

file(GLOB_RECURSE HDRS ${HDRS} include/*.h)
file(GLOB_RECURSE SRCS ${SRCS} src/*.c)
add_executable(rtv1 ${SRCS} ${HDRS})
target_include_directories(rtv1 PUBLIC include)
target_link_libraries(rtv1 PUBLIC ft mlx pthread
  "-framework AppKit" "-framework OpenGL")
