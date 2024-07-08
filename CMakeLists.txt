# 111 - 파일 명시.
# cmake_minimum_required(VERSION 3.0.0)
# project(my_lib VERSION 0.1.0 LANGUAGES C)

# add_executable(my_lib main.c string/my_string.c)
 
# set(CPACK_PROJECT_NAME ${PROJECT_NAME})
# set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
# include(CPack)

# 222 - 폴더 명시.
# cmake_minimum_required(VERSION 3.0.0)
# project(my_lib VERSION 0.1.0 LANGUAGES C)

# # string 디렉토리 안의 모든 .c 파일을 가져옴
# file(GLOB STRING_SOURCES "string/*.c")

# # 모든 .c 파일을 사용하여 실행 파일 생성
# add_executable(my_lib main.c ${STRING_SOURCES})

# # CPack 설정
# set(CPACK_PROJECT_NAME ${PROJECT_NAME})
# set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
# include(CPack)

# 333 - 전체 c 파일.
cmake_minimum_required(VERSION 3.0.0)
project(my_lib VERSION 0.1.0 LANGUAGES C)

file(GLOB ALL_SOURCES "*.c" "**/*.c")

# 모든 .c 파일을 사용하여 실행 파일 생성
add_executable(my_lib main.c ${ALL_SOURCES})

# CPack 설정
set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)