# ComputerNetworking
Notice: this project have been tested on Visual Studio 2022

## Preparing

You need to have these features:

`CMake` : download on the CMake official website

`vcpkg`

### Installing vcpkg


Step 1: Clone vcpkg repository:

```git clone https://github.com/microsoft/vcpkg.git```

Step 2: Run the boostrap: 

```cd vcpkg; .\bootstrap-vcpkg.bat```

Step 3: Set the environment variables: 

```$env:VCPKG_ROOT = "C:\path\to\vcpkg"```
```$env:PATH = "$env:VCPKG_ROOT;$env:PATH"```

## Run
Clone this repository and open it

```
git clone https://github.com/iAmHieu2012/ComputerNetworking.git
cd ComputerNetworking
```
Before building files, you need to change the macro in `Client.cpp`:

`#define SENDER_MAIL "abc@gmail.com"`

to the mail which you use to send request to server machine

## Build

Choose `vcpkg` to build projects

`Ctrl` + `Shift` + `B`  to build 3 subprojects `server`, `client`, `webcam`

The execute files built are placed in separate folders in `\build`

`curl` and `nlohmann-json` are auto-generate on your machine too.

## Run
Before running these execute files, remember:
	
+ put `server.exe` and `webcam.exe` into the same directory on the server machine

+ put `client.exe`(required) ,`credentials.json`(required, i've put it in the solution directory) and `token.json` (if missing you will be asked to get a new access_token, so you needn't care 'bout it) into the same directory on the client machine

if the `token.json` is missing/error, the client application will ask you to get the authorization code.
You must use this account to get the token: 
the mail of the client machine :
mail account: `hieudapchailo@gmail.com`
password: `Hieu.google.2012`

### On the server machine (Run as Administrator to works with WindowsServices)
```
server.exe
```
### On the client machine
```
client.exe
```

use `SENDER_MAIL` to send email to the client email `hieudapchailo@gmail.com` with:

	To: <__hieudapchailo@gmail.com__>

	Subject: <__Server's IP Address__>

	Body: <__one of the commands below__>

list of commands:

`SHUTDOWN`

`STARTPROCESS taskName.exe`

`KILLPROCESS taskName.exe`

`LISTPROCESS file.txt`

`STARTSERVICE svcName`

`STOPSERVICE svcName`

`LISTSERVICES file.txt`

`SCREENCAPTURE file.png`

`SENDFILE fileName.abc`

`TURNONCAMERA`

`TURNOFFCAMERA`

## How it works

you(SENDER_MAIL: you modify your own email)-->

-- send email of your order -->  Client(Mail: hieudapchailo@gmail.com)

-- send the task -->  Server

-- do the task and send result -->  Client

-- send email of the result -->  you(SENDER_MAIL)



