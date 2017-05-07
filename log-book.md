

Only for rooted devices: If you want the script to be run directly as a
command, place the script in **/system/bin** (or) **/system/xbin** . Then make the
file executable by running the following command:

```sh
    sh
    su
    mount -o rw,remount /system
    cp <script_path>/<script_name> /system/bin/<script_name>
    chmod 555 /system/bin/<script_name>
```

For example I have copied the script **"testmsg.sh"** to **/system/bin**, renamed it
to **"testmsg"** using the following commands:

```
    su/
    mount -o rw,remount /system
    cp /storage/sdcard0/sh/testmsg.sh /system/bin/testmsg
    chmod 555 /system/bin/testmsg (chmod +x did not work, giving me a bad mode error)
```

Now in the Terminal Emulator, just enter the name of the file and the script
will execute.


Iniciando o shell

```sh
    adb shell am start -n jackpal.androidterm/.Term
```
