# Docker_CPP

## Description 
Docker file to compile C++ code

## Build Container
```
docker build -t docker_cpp -f Dockerfile-development .
```

## Run Docker Container Environment
This docker will commmand will mound the current directory insside the /build directory.  The reason to mount the directory is to keep the compiled binery in the host OS.

### On Windows
```
docker run -v "c:\build:/build" docker_cpp
```

### On Linux
```
docker run -v "/src:/build" docker_cpp
```

## Compiling your code
Once inside the bash file execute 
```
g++ helloworld.cpp
```

## Run you code
```
./a.out
```

## Cleanup
```
exit
```

The a.out file will stay on your host OS after the container exits.