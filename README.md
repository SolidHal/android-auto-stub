## AndroidAutoStub

- stock AndroidAutoStub extracted from pixel
- custom built Google Search App and Google Speech Services Stubs

## Build (Generic AOSP)

*This assumes you already are getting microg on your device some other way.* 

add this to your manifests to use:
```
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
	  <project name="SolidHal/android-auto-stub" path="prebuilts/androidauto" remote="github" revision="master" />
</manifest>
```

then include the following line in your device.mk or common.mk:
```
PRODUCT_PACKAGES += AndroidAuto gappsstub speechservicestub
```
or you can also add it to your `vendor/$vendor/config/common.mk`

Now continue to "Get android auto setup" below

## Build lineageOS with Android Auto

*this method will include microg and Android Auto and the stubs automatically in your build*

I suggest using https://github.com/lineageos4microg/docker-lineage-cicd

see the following repo for an example device:
https://github.com/SolidHal/lineageos-microg-oneplus-lemonade

Now continue to "Get android auto setup" below

## Get android auto setup

- Install the latest android auto apk (you can find this online or get it with aurora store)
- Install google maps in the same way
- open google maps once, grant it location permissions. Just while in use is fine.
- android auto *should* just work now

if you get stuck on google maps permission, try pressing cancel instead of settings.

if you are having trouble with first time setup, I found it was helpful to setup the bluetooth connection to the car before plugging in the usb c.


## Sources

sources for custom built stubs with build instructions for each of the stubs:
https://github.com/SolidHal/SpeechServices-Package-Spoof
https://github.com/SolidHal/Gapp-Package-Spoof

## Thanks
big thanks to @dylangerdaly and the thread here https://github.com/microg/GmsCore/issues/897

