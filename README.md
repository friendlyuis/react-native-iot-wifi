# react-native-iot-wifi
Wifi configuration.
This library was written to config iot devices. With iOS 11 Apple introduced NEHotspotConfiguration class for wifi configuration. Library supports same functioanllity on ios and android.

## iOS
> Important
> IOTWifi uses NEHotspotConfigurationManager. To use the NEHotspotConfigurationManager class, you must enable the Hotspot Configuration capability in [Xcode](http://help.apple.com/xcode/mac/current/#/dev88ff319e7).

1. Drang an drop `IOTWifi.xcodeproj` to your workspace
2. [Link target](https://help.apple.com/xcode/mac/current/#/dev51a648b07) to `libIOTWifi.a` library
3. [Link target](https://help.apple.com/xcode/mac/current/#/dev51a648b07) to `NetworkExtension.framework` framework
4. [Enable](http://help.apple.com/xcode/mac/current/#/dev88ff319e7) `Hotspot Configuration`

## android


## Usage

```javascript
import Wifi from "react-native-iot-wifi";

Wifi.isAvaliable((avaliable) => {
  console.log(avaliable ? 'avaliable' : 'failed');
});

Wifi.getSSID((SSID) => {
  console.log(SSID);
});

Wifi.connect("wifi-name", (error) => {
  console.log(error ? 'error: ' + error : 'connected to wifi-name');
});

Wifi.removeSSID("wifi-name", (error)=>{
  console.log(error ? 'error: ' + error : 'removed wifi-name');
});
```