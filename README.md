LiveSDK.Android
===============

2/1/2014
Xamarin Binding Library for LiveSDK for Android

This project is an Android Java Bindings Library to expose a native Android jar to Xamarin. 

This project contains the livesdk.jar which is the LiveSDK for Android distributed by Microsoft Corporation.
https://github.com/liveservices/LiveSDK-for-Android
Version 5.5 was compiled and included in this project.

To update to future versions of the LiveSDK, compile latest from github and include in this project under Jars.

LiveSDK.Android.Sample is a sample Xamarin.Android application for illustrating usage.  Example;

		private void Login ()
		{
			Java.Util.ArrayList scopes = new Java.Util.ArrayList ();
			scopes.AddAll (new string[] { "wl.signin", "wl.skydrive_update", "wl.offline_access" });

			LiveAuthClient client = new LiveAuthClient(this, CLIENT_ID);
			client.Login (this, scopes, this);
		}
