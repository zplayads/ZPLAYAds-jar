### 1. Puts the jar, named zplayads-2.3.1.jar, into your project libs.
### 2. Add the picture into your project assets directory.

#### 2.1 **required** picture:
- zp_force_close_button.png: The little 'X' button image when ad is showing.
- zp_force_close_button_bg.png: The gray background of the little 'X' button.

#### 2.2 optional picture (you can ignore these pictures, if you do not integrat ZPLAYAds native ad)
- native_down_btn.png: The Chinese version of the picture shows "PLAY NOW".
- native_down_btn_en.png: The English version of the picture shows "PLAY NOW".
- native_landing_page_back_img.png: The back image in the native landingpage.

### 3. Register permissions to AndroidManifest.xml 
#### 3.1 **required** permissions
```
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

#### 3.2 optional permission
```
<uses-permission android:name="android.permission.REQUEST_INSTALL_PACKAGES"/>
```

### 4. Register components to AndroidManifest.xml
#### 4.1 **required** component
```
<activity
    android:name="com.playableads.presenter.PlayableADActivity"
    android:configChanges="orientation|screenSize|keyboardHidden"
    android:hardwareAccelerated="true"
    android:screenOrientation="portrait"
    android:theme="@android:style/Theme.NoTitleBar.Fullscreen" />
```

#### 4.2 optional component (you can ignore this component, if you do not integrat ZPLAYAds native ad)
```
<activity
    android:name="com.playableads.presenter.NativeAdLandingPageActivity"
    android:configChanges="orientation|screenSize|keyboardHidden"
    android:hardwareAccelerated="true"
    android:screenOrientation="portrait"
    android:theme="@android:style/Theme.NoTitleBar.Fullscreen" />
```