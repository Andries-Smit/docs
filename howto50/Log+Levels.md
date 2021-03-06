---
title: "Log Levels"
category: 'Monitoring & Troubleshooting'
space: "Mendix 5 How-to's"
---

Each application has a log and log-messages to monitor the health of the running of the application. Log levels are used to distinguish the log messages and to highlight the highest priority ones so that they can receive the immediate intervention they require. This How-To will therefore teach you how to configure the log levels for the various occurrence of logging within your application. You will start with the basics around logging and its uses. Moving onto the practices around configuring the log levels.

## 1\. Logging the basics

### 1.1 Log message

Log messages are a note that appears in the log of your Mendix application filled with an abundance of contextual information, such as:

*   The date/time created
*   The level
*   The node
*   A detailed message
*   A stack trace

**_Log Node_**

The log node name defines the source of the log message, for instance a log message from the email module, the log name would appear as **_“Email Module”._**

**_The message_**

Most messages in the log are auto-generated by the system for instance **_‘Mendix Runtime successfully started, the application is now available’_**. However for logging that have been created via microflow, log messages can be customized by the developer.

 ![](attachments/8782589/8946001.png)

Customized log messages are created by defining a template, in the example above the template for the message is:

**_‘Email not sent to customer {1}’_**

The template is the structure of the log’s message, and can be composed of parameters and free text. If we take the example above, when the error occurs we insert into the parameter placeholder **_‘{1}’_ **the customer’s full name. Therefore producing the log message **_‘Email not sent to customer John Smith’_**. This log message is now customized to data specific to the situation.

**The stack trace**

The stack trace is a list of method calls from the point when the application was started to the point where the exception was thrown.
In the modeler, log messages that include a stack trace are marked with a paperclip icon () and double-clicking them shows the stack trace.

### 1.2 The different levels

The log level defines the severity of the log message. In the modeler, this is represented by different colors and an icon. Current log levels used by Mendix are: 

<table><thead><tr><td class="highlight-grey confluenceTd" data-highlight-colour="grey"><strong>Option</strong></td><td class="highlight-grey confluenceTd" data-highlight-colour="grey"><strong>Icon</strong></td><td class="highlight-grey confluenceTd" data-highlight-colour="grey"><strong>Color</strong></td><td class="highlight-grey confluenceTd" data-highlight-colour="grey"><strong>When it’s used</strong></td></tr></thead><tbody><tr><td class="confluenceTd"><em>Trace</em></td><td class="confluenceTd"><em>&nbsp;</em></td><td class="confluenceTd"><em>&nbsp;</em></td><td class="confluenceTd"><em>More detailed information. These are only written to logs.</em></td></tr><tr><td class="confluenceTd"><em>Debug</em></td><td class="confluenceTd"><em>&nbsp;</em></td><td class="confluenceTd"><em>&nbsp;</em></td><td class="confluenceTd"><em>Detailed information, typically of interest only when diagnosing problems.</em></td></tr><tr><td class="confluenceTd"><em>Info</em></td><td class="confluenceTd"><em>&nbsp;</em></td><td class="confluenceTd"><em>&nbsp;</em></td><td class="confluenceTd"><em>Confirmation that things are working as expected.</em></td></tr><tr><td class="confluenceTd"><em>Warning</em></td><td class="confluenceTd"><img class="confluence-embedded-image image-center" src="attachments/8782589/8946006.png" data-image-src="attachments/8782589/8946006.png"></td><td class="confluenceTd"><span><em>Text is orange</em></span></td><td class="confluenceTd"><em>An indication that something unexpected happened, or indicative of some problem in the near future (e.g. ‘disk space low’). The application is still working as expected.</em></td></tr><tr><td class="confluenceTd"><em>Error</em></td><td class="confluenceTd"><img class="confluence-embedded-image image-center" src="attachments/8782589/8946007.png" data-image-src="attachments/8782589/8946007.png"></td><td class="confluenceTd"><span><em>Text is red</em></span></td><td class="confluenceTd"><em>Due to a more serious problem, the application has not been able to perform some function.</em></td></tr><tr><td class="confluenceTd"><em>Critical</em></td><td class="confluenceTd"><img class="confluence-embedded-image image-center" src="attachments/8782589/8946008.png" data-image-src="attachments/8782589/8946008.png"></td><td class="confluenceTd"><span><em><span>Text is white, background red</span></em></span></td><td class="confluenceTd"><em>A serious error, indicating that the application itself may be unable to continue running.</em></td></tr></tbody></table>

## 2\. Setting the log levels

Within this part of the how to you will learn how to configure the log levels of the logging messages produced by the system. The different levels highlighted above in section 1.2, can be applied to custom logging and to the predefined logging produced by the Mendix Business Modeller. This section will define how to configure both the log levels in custom logging and the predefined logging created by the Modeller.

### 2.1 Advanced features of the console

![](attachments/8782589/8946108.png)

1.  Open the console
2.  Click ‘Advanced’ to open the drop down list of advanced options
3.  On the list of options click ‘Set log levels…’

### 2.2 Configuring log levels

You can now select the level that which a log node will log messages as.

 ![](attachments/8782589/8946109.png)

1.  Set the relevant log node
2.  Click on the drop down list, in the log level column
3.  From the drop down list select the correct level

### 2.3 Configuring custom log levels

You can also set the level of log messages in ones that you have created via a microflow.

 ![](attachments/8782589/8946110.png)

1.  Open the relevant microflow, for which you intend to change its log message’s level.
2.  Double click on the ‘log message activity’
3.  From the drop list, in the log level row select the correct level 

## 3\. Related content

*   [Finding the Root Cause of Runtime Errors](Finding+the+Root+Cause+of+Runtime+Errors)
*   [Clearing Warning Messages in Mendix](Clearing+Warning+Messages+in+Mendix)
*   [Testing web services using SoapUI](Testing+web+services+using+SoapUI)
*   [Debugging Microflows](Debugging+Microflows)
*   [Common Mendix SSO Errors](Common+Mendix+SSO+Errors)
*   [Monitoring Mendix using JMX](Monitoring+Mendix+using+JMX)
*   [Debugging Java Actions](Debugging+Java+Actions)
