---
title: App Center Push for Unity Windows
description: Using Push in App Center
keywords: sdk, push
author: jwhitedev
ms.author: jawh
ms.date: 12/19/2018
ms.topic: article
ms.assetid: 74B832B4-C9C6-40C5-A693-473F385DC817
ms.service: vs-appcenter
ms.custom: sdk
ms.tgt_pltfrm: unity
---

# App Center Push

> [!div  class="op_single_selector"]
> * [Android](android.md)
> * [iOS](ios.md)
> * [UWP](uwp.md)
> * [Xamarin.Android](xamarin-android.md)
> * [Xamarin.iOS](xamarin-ios.md)
> * [Xamarin.Forms](xamarin-forms.md)
> * [React Native Android](react-native-android.md)
> * [React Native iOS](react-native-ios.md)
> * [macOS](macos.md)
> * [Cordova Android](cordova-android.md)
> * [Cordova iOS](cordova-ios.md)
> * [Unity Android](unity-android.md)
> * [Unity iOS](unity-ios.md)
> * [Unity Windows](unity-windows.md)

App Center Push enables you to send push notifications to users of your app from the App Center portal and relies on [Windows Notification Services](https://docs.microsoft.com/windows/uwp/controls-and-patterns/tiles-and-notifications-windows-push-notification-services--wns--overview) (WNS) to push notifications to the devices.

> [!NOTE]
> The device displays a toast only if the application is in background at the moment the Push is received.

## Add App Center Push to your app

Please follow the [Get started](~/sdk/getting-started/uwp.md) section if you haven't set up and started the SDK in your application.

### Enable App Center Push

[!include[](unity-enable.md)]


## Register your app for Windows Notification Services (WNS)

Before you can send notification using WNS, your app must be registered with the Windows Store. This will provide you with credentials for your app that App Center will use to authenticate with WNS. These credentials consist of a Package Security Identifier (SID) and an application secret key. To perform this registeration, you need to associate your app with the Windows Store in Visual Studio.

To register the app, you will need to export it as a project first. 
For this, on the Unity **Build Settings** tab, build the app and then open the built solution in **Visual Studio**.

[!include[](windows-wns.md)]

## Intercept push notifications

[!include[](unity-intercept.md)]

[!include[](unity-api-enable.md)]