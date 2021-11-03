<manifest versionCode="1" versionName="1.0" compileSdkVersion="30" compileSdkVersionCodename="11" coreApp="true" package="com.samsung.advp.imssettings" platformBuildVersionCode="30" platformBuildVersionName="11">
<uses-sdk minSdkVersion="30" targetSdkVersion="30"/>
<permission name="com.sec.android.voltesettings.permission.KEYSTRING" protectionLevel="0x3"/>
<permission name="com.sec.android.app.hiddenmenu.permission.KEYSTRING" protectionLevel="0x3"/>
<uses-permission name="android.permission.READ_PRIVILEGED_PHONE_STATE"/>
<uses-permission name="com.sec.imsservice.READ_IMS_PERMISSION"/>
<uses-permission name="com.sec.imsservice.WRITE_IMS_PERMISSION"/>
<uses-permission name="com.sec.imsservice.PERMISSION"/>
<uses-permission name="android.permission.READ_EXTERNAL_STORAGE"/>
<uses-permission name="android.permission.WRITE_EXTERNAL_STORAGE"/>
<uses-permission name="com.sec.imslogger.permission.SERVICE"/>
<uses-permission name="android.permission.READ_PHONE_STATE"/>
<uses-permission name="android.permission.MASTER_CLEAR"/>
<uses-permission name="com.sec.phone.permission.SEC_FACTORY_PHONE"/>
<uses-permission name="com.samsung.ims.permission.hdvoicesettinginfo"/>
<uses-permission name="com.sec.nsds.READ_NSDS_PERMISSION"/>
<uses-permission name="com.sec.nsds.WRITE_NSDS_PERMISSION"/>
<uses-permission name="android.permission.ACCESS_NETWORK_STATE"/>
<uses-permission name="android.permission.SYSTEM_ALERT_WINDOW"/>
<uses-permission name="com.sec.android.providers.iwlansettings.permission.WRITE_IWLANSETTINGS"/>
<uses-permission name="com.sec.android.providers.iwlansettings.permission.READ_IWLANSETTINGS"/>
<uses-permission name="com.sec.ims.nsds.READ_NSDS_PERMISSION"/>
<uses-permission name="com.sec.ims.nsds.WRITE_NSDS_PERMISSION"/>
<uses-permission name="com.sec.ims.entitlementconfigservice.READ_ENTITLEMENT_CONFIG_PERMISSION"/>
<uses-permission name="com.sec.ims.entitlementconfigservice.WRITE_ENTITLEMENT_CONFIG_PERMISSION"/>
<application theme="ImsSettingsTheme" label="IMS Settings" icon="res/drawable/icon.xml" allowBackup="false" extractNativeLibs="false" usesNonSdkApi="true">
<activity label="IMS Settings" name="com.samsung.advp.imssettings.MainActivity" exported="false" screenOrientation="1">
<intent-filter>
<action name="android.intent.action.MAIN"/>
</intent-filter>
</activity>
<activity name="com.samsung.advp.imssettings.ImsServiceSwitchActivity" screenOrientation="1"/>
<activity name="com.samsung.advp.imssettings.ImsProfileList" screenOrientation="1"/>
<activity name="com.samsung.advp.imssettings.ImsProfileEditor" screenOrientation="1"/>
<activity name="com.samsung.advp.imssettings.ISIMInfo" screenOrientation="1"/>
<activity name="com.samsung.advp.imssettings.IMSInfo" screenOrientation="1"/>
<activity name="com.samsung.advp.imssettings.SmkUpdatedInfo" screenOrientation="1"/>
<activity name="com.samsung.advp.imssettings.AudioCodecSelector" screenOrientation="1"/>
<activity name="com.samsung.advp.imssettings.ImsLogger"/>
<activity name="com.samsung.advp.imssettings.EntitlementReset"/>
<activity name="com.samsung.advp.imssettings.DebugScreen" screenOrientation="1"/>
<activity name="com.samsung.advp.imssettings.GlobalSettingsEditor" screenOrientation="1"/>
<activity name="com.samsung.advp.imssettings.FakeCapability" screenOrientation="1"/>
<activity name="com.samsung.advp.imssettings.DmConfigEditor" screenOrientation="1"/>
<activity name="com.samsung.advp.imssettings.SelfProvisioning" screenOrientation="1"/>
<activity name="com.samsung.advp.imssettings.CMStoreSettings" screenOrientation="1"/>
<activity name="com.samsung.advp.imssettings.HDVoiceSettings"/>
<activity label="IMS Settings" name="ImsSettingsLauncherActivity" permission="com.sec.imslogger.permission.SERVICE">
<intent-filter>
<action name="android.intent.action.MAIN"/>
<action name="com.sec.android.voltesettings.launcher"/>
<category name="android.intent.category.DEFAULT"/>
</intent-filter>
</activity>
<receiver name="com.samsung.advp.imssettings.SecretCodeReceiver" permission="com.sec.android.app.hiddenmenu.permission.KEYSTRING">
<intent-filter>
<action name="android.provider.Telephony.SECRET_CODE"/>
<data scheme="android_secret_code" host="467"/>
</intent-filter>
</receiver>
<receiver name="com.samsung.advp.imssettings.DialerCodeReceiver" permission="com.sec.android.voltesettings.permission.KEYSTRING">
<intent-filter>
<action name="android.provider.Telephony.SECRET_CODE"/>
<data scheme="android_secret_code" host="77467"/>
</intent-filter>
</receiver>
<receiver name="com.samsung.advp.imssettings.CmccVoLTEEnableReceiver" permission="com.sec.android.app.hiddenmenu.permission.KEYSTRING">
<intent-filter>
<action name="android.provider.Telephony.SECRET_CODE"/>
<data scheme="android_secret_code" host="865838378"/>
</intent-filter>
</receiver>
<uses-library name="imsmanager"/>
<uses-library name="sec_platform_library"/>
<uses-library name="vsimmanager" required="false"/>
<service name=".AudioCodecWidgetService" enabled="true" exported="false"/>
</application>
</manifest>
