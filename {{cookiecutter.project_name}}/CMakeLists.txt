cmake_minimum_required(VERSION 3.16)

project({{cookiecutter.project_name}} VERSION 0.0.1 LANGUAGES CXX)

set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_INCLUDE_CURRENT_DIR ON)

configure_file(app.rc.in app.rc)

find_package(Qt6 REQUIRED COMPONENTS Widgets)

qt_add_executable({{cookiecutter.project_name}}
    app.rc
    main.cpp
    mainwindow.cpp
    mainwindow.h
    mainwindow.ui
)

qt_add_resources({{cookiecutter.project_name}} "icons"
    PREFIX "/"
    FILES icons/qt.ico
)

target_link_libraries({{cookiecutter.project_name}} PRIVATE Qt6::Widgets)
