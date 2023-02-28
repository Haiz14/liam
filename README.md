# Goal: 
Upon installing termux a custom script must run every time termux is opened 

# Contents

[how-termux-apk-is-built-(only-relevant)](#how-termux-is-built)

# how-termux-is-built

When building the [apk](https://github.com/termux/termux-app) bootstrap packages is downloaded from url [app/build.gradle](https://github.com/termux/termux-app/blob/master/app/build.gradle#L185) and then stored in [main/cpp/termux-bootstrap.zip](https://github.com/termux/termux-app/blob/master/app/src/main/cpp/termux-bootstrap-zip.S). (then the bootstrap packages is stored inside the apk built) 

Then when the apk is first installed the bootstrap packages is unzipped and stored in `$PREFIX` (here's the relevant[file](https://github.com/termux/termux-app/blob/master/app/src/main/java/com/termux/app/TermuxInstaller.java#L380) 


