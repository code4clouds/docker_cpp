# Docker_CPP

## Description 
Docker file to compile C++ code

## Build Container
```
docker build -t docker_cpp -f Dockerfile-development .
```

## Run Docker Container Environment
This docker will commmand will mound the current directory insside the /build directory

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