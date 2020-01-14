# NU Horizon

# About 
Coming Soon...

# Navigation
* .
    * README.md - File contains meta information about the project, project structure, and coding conventions
    * ...

# Style Guide
* General Rules of Thumb
    * Include a purpose statement for all methods/functions
    * Include a signature for any non-typed language (Python)
    * No function/method should be longer than 20 lines.
    * One function/method for one purpose

## ROS Packages
All ROS Packages should conform to the following structure...

```
/package_name                   # Top Level package folder
    /msg                        # Contains all custom messages defined in this package
        CustomMsg.msg
        OtherCustomMsg.msg
    /srv                        # Contains all custom services for this package
        CustomService.srv 
    /action                     # Contains all custom actions for this package
        CustomAction.action     
    /launch                     # Contains all launchfiles for this package
        launch_node.launch

    # FOR C++ Packages
    /include/package_name       # Contains headerfiles for all custom classes
        custom_class.h
    /src                        # Contains implementations for all custom classes
        custom_class.cpp

    # For Python Packages
    /nodes                      # Contains executables for custom nodes
        custom_node 
    /src                        # Contains custom python modules used in this package      
        custom_module.py

    CMakeLists.txt              # Build Specification
    package.xml                 # Package Information
    README.md                   # Package Description (Discusses purpose of node(s) and provided topics/services/actions)
```

## C++
For all cpp files the formatter: [clang-format](https://www.kernel.org/doc/html/latest/process/clang-format.html) should be used.
Developers should use the `.clang-format` file in the top level of the directory. 

* How to use with ...
    * Eclipse : https://marketplace.eclipse.org/content/cppstyle
    * VSCode : https://code.visualstudio.com/docs/cpp/cpp-ide

If an ide exension doesnt exist the command-line applications can be used. 

## Python
For all python files the formatter: [black](https://black.readthedocs.io/en/stable/) should be used with default format settings.

* How to use with ...
    * VSCode : https://code.visualstudio.com/docs/python/editing#_formatting

If an ide exension doesnt exist the command-line applications can be used. 

## .msg/.srv/.action
When defining custom messages, services, and actions always...
* Comment Units for scalar quantities