# Docker for Android SDK 28 and NDK 21

Docker for Android SDK 28 with preinstalled SDK and NDK

> Edit from [docker-android-sdk/android-28](https://github.com/docker-android-sdk/android-28)

**Installed Packages**
```bash
# sdkmanager --list
  Path                                        | Version      | Description                                | Location
  -------                                     | -------      | -------                                    | -------
  build-tools;32.0.0                          | 30.0.2       | Android SDK Build-Tools 30.0.2             | build-tools/30.0.2/
  cmdline-tools;latest                        | 2.1          | Android SDK Command-line Tools (latest)    | cmdline-tools/latest/
  platform-tools                              | 30.0.4       | Android SDK Platform-Tools                 | platform-tools/
  platforms;android-28                        | 6            | Android SDK Platform 28                    | platforms/android-28/
  ndk;21.4.7075529                            | 21.4.7075529 | Android NDK 21                             | ndk/21.4.7075529/
```

**Usage**

- Interactive way
  ```bash
  $ docker run -it --rm --device /dev/kvm androidsdk/android-28:latest bash
  # check installed packages
  $ sdkmanager --list
  # You can also run other Android platform tools, which are all added to the PATH environment variable
  ```

- Non-interactive way
  ```bash
  # check installed packages
  $ docker run -it --rm androidsdk/android-28:latest sdkmanager --list
  # You can also run other Android platform tools, which are all added to the PATH environment variable
  ```