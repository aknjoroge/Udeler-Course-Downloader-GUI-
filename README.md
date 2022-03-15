# Udeler | Udemy Course Downloader (GUI)

### Warning

**Udemy has started to encrypt many of the course videos, so downloading them may be impossible/illegal because it involves decrypting DRM'd videos which opens up the author to DMCA takedowns/lawsuits.
If you use Udeler and some/all videos are skipped, please don't open a new issue or comment that the issue still exists.  All requests to bypass DRM/encryption will be ignored.**


# Disclaimer:

This software is WIP, the code is provided as-is and I am not held resposible for any legal issues resulting from the use of this program.

This software is intended to help you download Udemy courses for personal use only.  
Sharing the content of your subscribed courses is strictly prohibited under Udemy Terms of Use.  
Each and every course on Udemy is subjected to copyright infringement.
This software does not magically download any paid course available on Udemy, you need to provide your Udemy login credentials to download the courses you have enrolled in.  
Udeler downloads the lecture videos by simply using the source of the video player returned to the user by Udemy after proper authentication, you can also do the same manually. 
Many download managers use same method to download videos on a web page. This app only automates the process of a user doing this manually in a web browser.

# License

All code is licensed under the MIT license

```
1. Clone the project
2. Run npm install
3. Run npm start
```

</p></details>

### Build
<details><summary>Expand</summary>
<p>

Detect Platform:

```
npm run dist
```

Windows:

```
npm run build-win
```

Mac:

```
npm run build-mac
```

Linux:

```
npm run build-linux
```

Cross Platform:

```
npm run build
```

#### To force 32 bit build:

_Append "-- --ia32" to npm run command_

Example:

```
npm run build-win -- --ia32
```

</p></details>

### Debug
<details><summary>Expand</summary>
<p>
First run ```npm run install``` to download/setup the required libraries.

Now in Visual Studio Code press ```CTRL-SHIFT-P``` and type "Debug: Open launch.json".

Insert this:
```
{
    "version": "0.2.0",
    "configurations": [
        {
            
            "name": "Launch",
            "type": "node",
            "request": "launch",
            "program": "${workspaceRoot}/index.js",
            "stopOnEntry": false,
            "args": [],
            "cwd": "${workspaceRoot}",
            "preLaunchTask": null,
            "runtimeExecutable": "${workspaceRoot}/node_modules/.bin/electron.cmd",
            "runtimeArgs": [
                ".",
                "--enable-logging",
                "--debug"
            ],
            "env": {},
            "console": "internalConsole",
            "sourceMaps": false,
            "outDir": null
        },
        {
            "name": "Attach",
            "type": "node",
            "request": "attach",
            "port": 5858,
            "address": "localhost",
            "restart": false,
            "sourceMaps": false,
            "outDir": null,
            "localRoot": "${workspaceRoot}",
            "remoteRoot": null
        }
    ]
}
```

(For MacOS/Linux, remove the .cmd from the runtimeExecutable.)

</p></details>

 
Udeler is free and without any ads. If you appreciate that, please consider donating to the Developer.
 