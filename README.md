CertUnpinning
----------------

# Introduction
This is a hook plugin used by [VirtualHook](https://github.com/rk700/VirtualHook). It hooks some Java APIs that are used for getting device info, and all the values are hard-codeded as a demo.

Currently the following methods are hooked:

- android.bluetooth.BluetoothAdapter.getAddress()
- android.telephony.gsm.GsmCellLocation.getCid()
- android.telephony.gsm.GsmCellLocation.getLac()
- android.location.Location.getLatitude()
- android.location.Location.getLongitude()
- android.telephony.TelephonyManager.getDeviceId()
- android.telephony.TelephonyManager.getLine1Number()
- android.telephony.TelephonyManager.getSimOperator()
- android.telephony.TelephonyManager.getSimSerialNumber()
- android.telephony.TelephonyManager.getSubscriberId()
- android.net.wifi.WifiInfo.getBSSID()
- android.net.wifi.WifiInfo.getSSID()
- android.net.wifi.WifiInfo.getIpAddress()
- android.net.wifi.WifiInfo.getMacAddress()

And these system property values are changed as well:

- ro.serialno
- ro.product.brand
- ro.product.device
- ro.build.tags
- ro.product.model
- ro.product.manufacturer

# Usage
Build and push the output apk to `/sdcard/io.virtualhook/patch.apk`. Then add and start applications in VirtualHook.
