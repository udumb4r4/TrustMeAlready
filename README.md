## TrustMeAlready 
An Xposed module to disable SSL verification and pinning on Android using the excellent technique provided by [Mattia Vinci](https://techblog.mediaservice.net/2018/11/universal-android-ssl-check-bypass-2/). The effect is system-wide.

### Requirements
* An Xposed-compatible hooking system. 
    * [LSPosed](https://github.com/LSPosed/LSPosed) (Android 12)  

### Tested
* Android 12.0, ARM64, LSPosed 1.8.3

### Troubleshooting
* Some apps implement custom certificate checking, bypassing this hook. Try sniffing Chrome traffic, if you don't get an invalid certificate error then this module is working as it should
* Check your LSPosed logs, chances are this module couldn't hook the correct method.
