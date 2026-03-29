# Setup

## Device / Emulator Setp

## Usefult Softwares

- `waydroid`
- `genymotion`

## Connection with `waydroid`

- start the waydroid ( from apps or )

   ```bash
      waydroid session start
      waydroid show-full-ui
   ```

- enable adbd ( android build tool bridge)

  - ```bash
       waydroid shell
    ```

  - from the shell - enable adb over tcp

    ```bash
       setprop persist.adb.tcp.port 5555
      stop adbd
      start adbd
      exit
    ```

- get waydroid ip with `waydroid status` (eg: 192.168.240.112)
- connect from adb
  - `adb connect 192.168.240.112`
  - allow permisson from waydroid app
  - check with `adb devices`

- if we get error
  - clean up & reconnect

  - ```bash
        rm -rf ~/.android/adbkey*
        adb kill-server
        adb start-server
    ```

- to stop `waydroid session stop`

## Connecting with `Genimotion` - Not working well

- donwload & run the installer
  - `bash genymotion-3.9.0-linux_x64.run`
- sing up & singin
  - kbdrreddy8 test
- start the Genymotion
- change adb tools to custom from settings
  - `/home/ravinder/Android/Sdk`
- create virtual device in Genymotion & Play

## Turorials / Docs

- [Rahul Pandey](https://www.youtube.com/watch?v=KLuiX1oHBII&list=PL7NYbSE8uaBCMVBVg6cskGzdYguj3CUP-)
  - [Code](https://github.com/rpandey1234/AndroidTippy)

- [Jetpack](https://developer.android.com/codelabs/jetpack-compose-basics)

## Note

- Views / Layout can be created in 2 ways
  1. androidx ( XML )
     - to create androidx(XML) views project
       - android studio -> new -> project -> `Empty Views Activity` -> give name & path

  2. jetpack  ( composables ) : modern way
     - to create jetpack project
       - android studio -> new -> project -> `Empty Activity` -> give name & path
