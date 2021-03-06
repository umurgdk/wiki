# libinput

Provides an high level api for [udev](/linux/programming/input/libudev) usage. It listens for device changes and events coming from udev and let the client know. 

## Device Files

libinput doesn't open device files itself, instead client program should provide file open and closing functions to pass file handles to libinput . Reading and writing operations to device files requires privileges, in case the client program has the priviledges it can open the files itself. If you don't want client program to have priviledges, file handles can be acquired by [logind's dbus api](/linux/programming/logind#dbus-api), which requires the client program to create a session and then take over the control of the device.

1. Find the session
2. Take control of the session
3. Take control of the device -- this sends a file handle in response

### Useful Links

* [Session implementation in rust](https://github.com/Smithay/smithay/blob/master/src/backend/session/dbus/logind.rs#L79)
