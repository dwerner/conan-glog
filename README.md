# conan-glog

[Conan.io](https://conan.io) package for Google's glog logging library

## Build packages

Download conan client from [Conan.io](https://conan.io) and run:

    $ python build.py
    
## Upload packages to server

    $ conan upload glog/0.13.3@dwerner/testing --all
    
## Reuse the packages

### Basic setup

    $ conan install glog/0.13.3@dwerner/testing/
    
### Project setup

If you handle multiple dependencies in your project is better to add a *conanfile.txt*
    
    [requires]
    glog/0.13.3@dwerner/testing

    [options]
    glog:shared=true # false
    
    [generators]
    txt
    cmake

Complete the installation of requirements for your project running:</small></span>

    conan install . 

Project setup installs the library (and all his dependencies) and generates the files *conanbuildinfo.txt* and *conanbuildinfo.cmake* with all the paths and variables that you need to link with your dependencies.
