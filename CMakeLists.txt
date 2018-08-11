cmake_minimum_required(VERSION 3.9)
project(ft_printf)

set(CMAKE_CXX_STANDARD 11)

add_executable(ft_printf
        ft_printf.c libftprintf.h)

add_library(libft STATIC IMPORTED)
set_property(TARGET libft PROPERTY IMPORTED_LOCATION ${CMAKE_SOURCE_DIR}/libft/libft.a)
target_link_libraries(ft_printf libft)