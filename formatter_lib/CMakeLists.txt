cmake_minimum_required(VERSION 3.4) # указывается необходимая минимальная версия cmake
project(formatter_lib)              # Задаётся имя проекта

set(CMAKE_CXX_STANDARD 11)          # Указывается требуемая версии стандарта С++
set(CMAKE_CXX_STANDARD_REQUIRED ON) # Указывается, что данное требование к стандарту обязательно

add_library(formatter_lib STATIC formatter.cpp)               # Создается  статическую библиотеку, тк она содержится в пректе.
target_include_directories(formatter PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})  # Указывается cmake где искать заголовочные файлы для библиотеки из предыдущей строчки
