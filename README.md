# PopupTranslator


## Description

Simple translator applet that will allow to display the translation 
of any selected text from any application on a system in a popup.

## Dependencies

**If one or more of these dependencies are missing in your system, you will not be able to use this applet.**

### xsel command

XSel is a command-line program for getting and setting the contents of the X selection.

- Debian and Archlinux based distributions: The package is called **xsel**.

### xdg-open command

Open a URI in the user's preferred application that handles the respective URI or file type.

Debian and Archlinux based distributions: This command is installed with the package called **xdg-utils**. Installed by default in modern versions of Linux Mint.

### Python 3

It should come already installed in all Linux distributions.

### requests Python 3 module

Requests allow you to send HTTP/1.1 requests. You can add headers, 
form data, multi-part files, and parameters with simple Python 
dictionaries, and access the response data in the same way. It's powered
 by httplib and urllib3, but it does all the hard work and crazy hacks 
for you.

Debian and Archlinux based distributions: This command is installed with the package called **xdg-utils**. Installed by default in modern versions of Linux Mint.
Debian based distributions: The package is called **python3-requests**. Installed by default in modern versions of Linux Mint.
Archlinux based distributions: The package is called **python-requests**.

**After installing any of the missing dependencies, Cinnamon needs to be restarted**
**Note:** I don't use any other type of Linux 
distribution (Gentoo based, Slackware based, etc.). If any of the 
previous packages/modules are named differently, please, let me know and
 I will specify them in this help file.

## Usage

There are 4 *translations mechanisms* (**Left click**, **Middle click**, **Hotkey #1** and **Hotkey #2**). Each translation mechanism can be configured with their own service providers, language pairs and hotkeys.

**First translation mechanism (Left click):** Translates any selected text from any application on your system. A hotkey can be assigned to perform this task.
**First translation mechanism (Ctrl + Left click):** Same as **Left click**, but it will bypass the translation history. A hotkey can be assigned to perform this task.
**Second translation mechanism (Middle click):** Same as **Left click**.
**Second translation mechanism (Ctrl + Middle click):** Same as Ctrl + **Left click**.
**Third translation mechanism (Hotkey #1):** Two hotkeys can be configured to perform a translation and a forced translation.
**Fourth translation mechanism (Hotkey #2):** Two 
hotkeys can be configured to perform a translation and a forced 
translation.
All translations are stored into the translation history. If a string of
 text was already translated in the past, the popup will display that 
stored translated text without making use of the provider's translation 
service.

## About translation history

I created the translation history mechanism mainly to avoid the abuse of the translation services.

If the Google Translate service is "abused", Google may block 
temporarily your IP. Or what is worse, they could change the translation
 mechanism making this applet useless and forcing me to update its code.
If the Yandex Translate service is "abused", you are "wasting" your 
API keys quota and they will be blocked (temporarily or permanently).
In the context menu of this applet is an item that can open the folder 
were the translation history file is stored. From there, the translation
 history file can be backed up or deleted.

**NEVER edit the translation history file manually!!!**
**If the translation history file is deleted/renamed/moved, Cinnamon needs to be restarted.**

## How to get Yandex translator API keys

Visit one of the following links and register a Yandex account (or use one of the available social services).
English: <https://tech.yandex.com/keys/get/?service=trnsl>
Russian: <https://tech.yandex.ru/keys/get/?service=trnsl>

Once you successfully finish creating your Yandex account, you can 
visit the link provided several times to create several API keys. **DO NOT ABUSE!!!**
Once you have several API keys, you can add them to Popup Translator's settings window (one API key per line).

### Important notes about Yandex API keys

The API keys will be stored into a preference. Keep your API keys backed up in case you reset Popup Translator's preferences.
**NEVER make your API keys public!!!** The whole 
purpose of going to the trouble of getting your own API keys is that the
 only one "consuming their limits" is you and nobody else.
With each Yandex translator API key you can translate **UP TO** 1.000.000 (1 million) characters per day **BUT NOT MORE** than 10.000.000 (10 millions) per month.

## Applets/Desklets/Extensions (a.k.a. xlets) localization

If this xlet was installed from Cinnamon Settings, all of this xlet's localizations were automatically installed.
If this xlet was installed manually and not trough Cinnamon 
Settings, localizations can be installed by executing the script called **localizations.sh** from a terminal opened inside the xlet's folder.
If this xlet has no locale available for your language, you could create it by following the following instructions. [Wiki](https://github.com/Odyseus/CinnamonTools/wiki/Xlet-localization)