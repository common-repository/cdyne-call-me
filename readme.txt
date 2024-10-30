=== Plugin Name ===
Contributors: HowdyMedia
Donate link: http://cdynecallme.howdymedia.com/donate/
Tags: call center, cdyne, call me, widget, phone, telemarketing, announcement, text to speech, text to say, answering machine, call in, call, phone notify,phonenotify, click to call, surveys, survey, poll, polls, school, press one, schedules, rsvp
Requires at least: 2.8.4
Tested up to: 3.3.1
Stable tag: 1.0

Easily add a 'Call Me' button to your website and create a call center with menus and number forwarding!

== Description ==

**CDYNE Call Me WordPress Plugin**
Create a call center or answering system complete to handle up to 5000 calls per minute with touch-tone menus and number forwarding utilizing CDYNE’s Phone Notify!&reg; service.

Potential Uses:

* Movie/Concert/Venue/Church Schedules & Show Times
* Business/Corporate Call Centers
* City or School Announcements and Cancellations
* Political Campaign Announcements
* Department Routing
* Touch-tone Polls/Surveys/Questionnaires
* Community Calendars
* RSVP By Phone

In order to use this plugin, you must set up an [account with CDYNE to acquire an API key](http://www.cdyne.com/products/phone-notify.aspx). You can apply for a free Trial key as well.

Visit the plugin webpage for the most up-to-date information:
[http://cdynecallme.howdymedia.com/](http://cdynecallme.howdymedia.com/)

== Installation ==

The plugin is divided in to two sections, what is displayed on your website and the configuration. Since this is a widget, you can create multiple independent widgets all with different scripts and configurations. On our right sidebar, we have two widget examples running completely different types of scripts. The first features a full key-press navigation, and the second is simply a message that plays once and disconnects the call.

**1. Installation**
From your WordPress admin section, click ‘Add New’ from the ‘Plugins’ section. In the search box, enter ‘CDYNE Call Me’ and submit. The plugin should appear at the top, it will show H.O.W.D.Y. Media as the author. Click install. After the plugin is installed, make sure to activate it from the Plugins section.

**2. Adding the Widget to a Sidebar**
From your WordPress admin section, click ‘Widgets’ from the ‘Appearance’ section. If installation was successful, a widget named CDYNE Call Me should appear in your widget box. Simply drag the widget to whichever sidebar that the widget should appear on.

**3. Widget Options**
The top section in the widget allows you to define the title, add your own HTML or text, and define the submit button. This gives you full control over what to show in the sidebar.

The bottom section contains all the CDYNE Phone Notify! settings, as well as your TextToSay (TTS) script. In order for the plugin to work, the API Key, Caller ID Number, Caller ID Name, and the TTS must be filled in. If your plugin does nothing, chances are you have not filled these fields in properly.

**API Key** - Given to you from CDYNE, this allows you access to their services. Trial keys are available, so you do not need to purchase anything to try this out on your own website. [Click here to get an API Key](http://www.cdyne.com/products/phone-notify.aspx).

**TextToSay Script** - Your message or script, complete with support for [advanced commands](http://cdynecallme.howdymedia.com/advanced-commands).

**Voice** - Various voices available which will read your script, listed by name with age and language support.

**Caller ID Number** - This is the phone number to display to the receiver of the call. This must be at least a 10 digit number.

**Caller ID Name** - The name to be displayed to the receiver of the call.

**Transfer Number *(Optional)*** - If you do not specify a transfer number using the [advanced commands](http://cdynecallme.howdymedia.com/advanced-commands), you can set a general number that will forward the call to the number entered. This must be at least a 10 digit number.

**4. TextToSay (TTS) Script**
To simply have a message read to the caller, enter your text making sure to use proper punctuation and spelling. Some words or names may not sound right, so you might need to change them to something more phonetically written. For instance, CDYNE isn’t a word, so using ‘c dine’ will ensure it is pronounced properly. Commas insert a slight pause, but to increase the pause, use the advanced command for playing silence.

[Advanced commands](http://cdynecallme.howdymedia.com/advanced-commands) can be inserted in to your script to control both the flow and how to handle key presses. Below is the script used on the ‘Call Us 24-7′ widget on our sidebar. Visit the link to see a full set of commands available.

`~\ActOnDigitPress(false)~
~\ClearDTMF()~
~\AssignDTMF(0|forward)~
~\AssignDTMF(1|about)~
~\AssignDTMF(2|install)~
~\AssignDTMF(3|support)~
~\AssignDTMF(4|top)~
~\ActOnDigitPress(true)~
~\SetVar(RepeatCount|0)~
Hello. This is an example of the C dine Call Me plugin for WordPress.
~\PlaySilence(1)~
~\Label(top)~
Press 1 to hear about the plugin, press 2 to hear about installation, press 3 to be forwarded to a live person, or press 4 to repeat this message. Hang up at any time to end this call.
~\WaitForDTMF(5)~
~\IncreaseVariable(RepeatCount|1)
~\GotoIf(RepeatCount|3|goodbye)~
~\Goto(top)~
~\Label(about)~
~\SetVar(RepeatCount|0)~
This call is powered by a WordPress plugin using C dines PhoneNotify service, which enables you to create your own call center for community calendars, department routing, and more.
~\PlaySilence(2)~
~\Goto(top)~
~\Label(install)~
~\SetVar(RepeatCount|0)~
Installation can be done automatically from your WordPress administration area.
~\PlaySilence(1)~
Simply click, add plugin, from the left hand sidebar and search for C Dine Call Me.
~\PlaySilence(1)~
Once installed, remember to activate the plugin.
~\PlaySilence(1)~
From there, under the appearance section, add the widget to a sidebar and configure as needed.
~\PlaySilence(2)~
~\Goto(top)~
~\Label(forward)~
~\Label(support)~
You are being forwarded to a support specialist.
~\TransferTo(13154698414)~
~\Goto(support)~
~\Label(goodbye)~
Goodbye.
~\EndCall()~`

== Frequently Asked Questions ==

= Where can I get an API Key? =
You can visit the CDYNE website to purchase or get a trial API key.
[http://www.cdyne.com/products/phone-notify.aspx](http://www.cdyne.com/products/phone-notify.aspx)

= How much does CDYNE's PhoneNotify!&reg; service cost? =
The pricing as of writing this was $9.99 a month for the service, plus a per minute rate depending on the monthly volume of minutes. This is a pay-as-you-go service, so you can stop anytime. For actual pricing, visit the following link and click the 'Pricing' button.
[http://www.cdyne.com/products/phone-notify.aspx](http://www.cdyne.com/products/phone-notify.aspx)

= Where can I find more example TextToSay scripts? =
The CDYNE website has some great examples available which can help you get running.
[http://cdynecallme.howdymedia.com/examples/](http://cdynecallme.howdymedia.com/examples/)

= I entered my own phone number, but didn't get a call =
You can't have the widget call the same number as what you provided for your Caller ID Number. Make sure to test using two phones. If you don't have a second phone available, you can get a free phone number from Google Voice.

= I entered a valid phone number different from the Caller ID Number, but didn't get a call =
Be sure that you have properly entered your API Key, Caller ID Number, Caller ID Name, and included a TextToSay (TTS) script. If these fields are set up incorrectly, you will not be able to process incoming calls. If you are using advanced commands, try backing up your script to a text document on your computer and entering a simple script with a single line of text and no commands.

= Can I use prerecorded messages rather than the computerized voice? =
It is possible to both upload and record unlimited WAV audio files, but this widget at this time doesn't directly support uploading audio files. There are advanced commands that allow you to record messages through your phone which then can be used in your TTS script.

Due to the complexity of managing the audio files, a new section would have to be added to the Wordpress backend outside of the widget area. This is something that is being considered for future versions. As a Phone Notify! subscriber, you are free to use other applications which can handle such tasks.

= Can I use this to robocall (make automated calls) using a phone number list? =
Technically, this is possible with CDYNE's Phone Notify! service, but this plugin doesn't directly support number lists and isn't set up to automatically call out. This is something that is being considered for future versions. As a Phone Notify! subscriber, you are free to use other applications which can handle such tasks.

== Screenshots ==

1. Widget Configuration
2. Sidebar Widget

== Upgrade Notice ==
This section intentionally left blank.

== Changelog ==

= 1.0 - 04/11/2012 =
* Initial release

== Support ==
* [Plugin Homepage](http://cdynecallme.howdymedia.com/)