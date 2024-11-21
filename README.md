# ComputerNetworking
Notice: this project have been tested on Visual Studio 2022

## Preparing

You need to have these features:

`CMake` : download on the CMake official website

`vcpkg`


Clone vcpkg repository:

```git clone https://github.com/microsoft/vcpkg.git```
Run the boostrap: 

```cd vcpkg; .\bootstrap-vcpkg.bat```

Set the environment variables: 

```$env:VCPKG_ROOT = "C:\path\to\vcpkg"```
```$env:PATH = "$env:VCPKG_ROOT;$env:PATH"```
Clone this repository and open it

```git clone https://github.com/iAmHieu2012/ComputerNetworking.git```
```cd ComputerNetworking```

## Build

`Ctrl` + `Shift` + `B`  to build 3 subprojects `server`, `client`, `webcam`

The execute files are built in separate folders in `\build`

`curl` and `nlohmann-json` are auto-generate on your machine too.

## Run
Before running these execute files, remember to put server.exe and webcam.exe into the same directory
### On the server machine (Run as Administrator to works with WindowsServices)
```
server.exe
```
### On the client machine
```
client.exe
```
list of commands:

```SHUTDOWN```

```STARTPROCESS taskName.exe```

```KILLPROCESS taskName.exe```

```LISTPROCESS file.txt```

```STARTSERVICE svcName```

```STOPSERVICE svcName```

```LISTSERVICES file.txt```

```SCREENCAPTURE file.png```

```SENDFILE fileName.abc```

```TURNONCAMERA```

```TURNOFFCAMERA```



