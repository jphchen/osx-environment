# Tools
- visual studio code https://code.visualstudio.com/download latest
- intellij / webstorm eap https://www.jetbrains.com/resources/eap latest
- sourcetree https://www.sourcetreeapp.com/download-archives v2.7.6
- homebrew https://brew.sh latest
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
- nvm latest
```
brew install nvm

add to ~/.profile

export NVM_DIR="$HOME/.nvm"
[ -s "/usr/local/opt/nvm/nvm.sh" ] && . "/usr/local/opt/nvm/nvm.sh"  # This loads nvm
[ -s "/usr/local/opt/nvm/etc/bash_completion" ] && . "/usr/local/opt/nvm/etc/bash_completion"  # This loads nvm bash_completion
```
- nodejs
```
nvm install node
```
- yarn
```
brew install yarn
``` 
- sdkman https://sdkman.io latest
```
curl -s "https://get.sdkman.io" | bash

source "$HOME/.sdkman/bin/sdkman-init.sh"
```
- java sdk
```
sdk install java
```
- android sdk
```
brew cask install android-studio
brew cask install android-sdk
brew cask install android-ndk

update env
echo "export ANDROID_HOME=/usr/local/share/android-sdk" >> ~/.profile
echo "export ANDROID_SDK_ROOT=/usr/local/share/android-sdk" >> ~/.profile
echo "export ANDROID_NDK_HOME=/usr/local/share/android-ndk" >> ~/.profile
echo "export PATH=$ANDROID_SDK_ROOT:$ANDROID_SDK_ROOT/emulator:$ANDROID_SDK_ROOT/platform-tools:$PATH" >> ~/.profile
touch ~/.android/repositories.cfg

*************************************************************************
For manual SDK, AVD, and project management, please use Android Studio.
For command-line tools, use tools/bin/sdkmanager and tools/bin/avdmanager
*************************************************************************

https://developer.android.com/studio/command-line/sdkmanager
sdkmanager --update
sdkmanager "platform-tools" "platforms;android-28"
sdkmanager --install "system-images;android-28;google_apis;x86"

https://developer.android.com/studio/command-line/avdmanager
avdmanager --verbose create avd --force --name "pixel_9.0" --device "pixel" --package "system-images;android-28;google_apis;x86" --tag "google_apis" --abi "x86"

avdmanager list avd
echo "alias pixel_9.0='emulator @pixel_9.0 -no-boot-anim -netdelay none -no-snapshot -wipe-data -skin 1080x1920 &'" >> ~/.profile
```

# Environment
## ssh
```
ssh-add ~/.ssh/some-ssh-key
```
## finder show/hidden files
```
alias showFiles='defaults write com.apple.finder AppleShowAllFiles YES;killall Finder /System/Library/CoreServices/Finder.app'
alias hideFiles='defaults write com.apple.finder AppleShowAllFiles NO; killall Finder /System/Library/CoreServices/Finder.app'
```
