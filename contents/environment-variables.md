# ENVIRONMENT VARIABLES
## Create a environment plist file.

```sh
$ sudo vim environment.plist
```


#### [environment.plist]

```sh
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
  <key>Label</key>
  <string>my.startup</string>
  <key>ProgramArguments</key>
  <array>
    <string>sh</string>
    <string>-c</string>
    <string>
      launchctl setenv <ENV1> <path1>
      launchctl setenv <ENV2> <path2> 
    </string>
  </array>
  <key>RunAtLoad</key>
  <true/>
</dict>
</plist>
```

##  Load environment with startup

```sh
$ cp environment.plist /Library/LaunchAgents/
```