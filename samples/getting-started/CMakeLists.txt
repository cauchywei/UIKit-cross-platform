cmake_minimum_required(VERSION 3.16)
project(DemoApp LANGUAGES C CXX Swift)
add_subdirectory("../../" UIKit)

add_library(DemoApp SHARED 
    ./DemoApp/ViewController.swift
    ./DemoApp/androidMain.swift
    ./DemoApp/AppDelegate.swift
)

target_link_libraries(DemoApp PRIVATE UIKit JNI SDL)