---
title: "How to Build a Mendix Hybrid Mobile App for Windows Phone"
space: "Mendix 6 How-to's"
category: "Mobile"
tags: []
---

## 1 Introduction

You may have tried to build a hybrid app package for Windows Phone, and found out this is not possible in the cloud portal. You can do this by building the Phonegap Build package yourself.

**This how-to will teach you how to do the following:**

* Create a Windows Phone app package.

## 2 Prerequisites

Before starting this how-to, make sure you have completed the following prerequisites:

* A Mendix App with mobile support running in the Mendix Cloud, either in a Free App or on a licensed cloud node
* An account for Adobe PhoneGap Build. You can sign up for an account [here](https://build.phonegap.com/plans)

## 3 Building the Windows Phone Package

### 3.1 Creating the Phonegap Build package

To create a Phonegap Build package using a provided template, follow these steps:

1. Download the Phonegap Build template [here (55KB)](./attachments/WP8_Phonegap_Build_Template.zip).
2. Extract the archive so you can change some files within it. <br>
3. Replace these variables in the `config.xml` file:
    * {{identifier}} - The app identifier. Must be unique for your application and must be reverse-domain name style (e.g. com.yourcompany.yourapp)
    * {{version}} - A major/minor/patch style version for the app with three numbers. For example 0.0.1
    * {{name}} - The name of your app
    * {{description}} - The description of your app

    After changing these variables, the `config.xml` will look similar to this:
    ```
    <?xml version="1.0" encoding="UTF-8" ?>
        <widget xmlns = "http://www.w3.org/ns/widgets"
            xmlns:gap = "http://phonegap.com/ns/1.0"
            id        = "com.mendix.sampleapp"
            version   = "1.0.0" >

        <name>My Sample App</name>

        <description>The Sample WP8 App</description>

        .....
    ```
4. Save the file.
5. Open the `index.html` file and change the `{{url}}` to the address where your application is
running (for example, `https://com.mendixcloud.myapp`).
6. Save the file. The part where the URL is used will now look similar to this:
    ```
    ...

    document.addEventListener("deviceready", function() {
        mxapp.initialize("https://com.mendixcloud.myapp", enableOffline, requirePin);
    });

    ...
    ```
To create an archive with these changes, follow these steps:

1. Select all the files and directories you extracted.
2. Right click the selection and select `Send to compressed folder`. This will create a new archive file that is ready for Phonegap Build.

### 3.2 Build the Windows Phone App

To build the Windows Phone app, follow these steps:

1. Log in to [Phonegap Build](https://build.phonegap.com/) and upload the archive you created in the previous section. This will trigger a build for Windows Phone, so sit bad back and relax while your build archive is being created.
2. When the build is finished, download the Windows Phone app by clicking the `xap` button.

You can deploy this xap file to the Windows store, or use it to test the app on a device.

## 4 Related Content
* [How to Deploy Your First Hybrid Mobile App](Deploy+your+first+Hybrid+Mobile+App)
* [How to Publish a Mendix Hybrid Mobile App in Mobile App Stores](Publishing+a+Mendix+Hybrid+Mobile+App+in+Mobile+App+Stores)
* [How to Debug a Hybrid Mobile Application](Debug+a+Hybrid+Mobile+Application)
* [Push Notifications](Push+Notifications)
