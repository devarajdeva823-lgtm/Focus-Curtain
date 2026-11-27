# Focus Curtain

**Version:** 2.4  
**Author:** Naveen Kumar M  
**Organisation:** EnAble India

Focus Curtain automates NVDA's built-in Screen Curtain according to the application that currently has focus. You can add individual applications to a saved list, so Screen Curtain is enabled when you move to one of those applications and disabled when you move to an application that is not on the list. You can also enable Screen Curtain for all applications.

## Author and organisation

**Naveen Kumar M**  
EnAble India

**Address:**  
Survey No. 9, Purva Gainz, 2nd Floor,  
Beratana Agrahara, Lavakusha Nagar, Hosur Main Road,  
Bengaluru, Karnataka 560100, India.

**Website:** [https://www.enableindia.org/](https://www.enableindia.org/)

## Features

- Automatically enables Screen Curtain when focus moves to an application in your selected application list.
- Automatically disables Screen Curtain when focus moves to an application that is not selected.
- Provides an all-applications mode that keeps Screen Curtain enabled across applications.
- Saves the selected application list and all-applications mode in your NVDA configuration folder, so these settings are retained when NVDA restarts.

## Keyboard shortcuts

### NVDA+G — Add or remove the current application

Move focus to the application you want to manage and press **NVDA+G**. If the application is not in the list, Focus Curtain adds it. If it is already in the list, Focus Curtain removes it. The add-on announces the action.

When an application is added, Screen Curtain automation is enabled. Screen Curtain is then turned on or off as application focus changes, according to the saved list.

### NVDA+H — Toggle Screen Curtain for all applications

Press **NVDA+H** to turn on Screen Curtain for all applications. Press it again to turn Screen Curtain off and leave all-applications mode.

**Important:** Turning all-applications mode off also clears the per-application selection list. You will need to add applications again with NVDA+G if you want to use per-application automation.

## How application-based automation works

1. Switch to the application you want Screen Curtain to cover.
2. Press NVDA+G to add that application to the list.
3. Switch to another application. Screen Curtain is enabled for applications in the list and disabled for applications that are not in the list.
4. To remove an application from the list, focus that application and press NVDA+G again.

The add-on identifies applications using the application name reported by NVDA. It does not provide a graphical settings dialog or a browseable list of saved applications.

## Screen Curtain behaviour and limitations

- Focus Curtain controls NVDA's built-in Screen Curtain. NVDA's Screen Curtain covers the entire display; it does not black out only the focused application window.
- The add-on changes Screen Curtain based on application focus. It does not provide separate curtains for individual windows within the same application.
- Application identification depends on NVDA being able to obtain an application name for the focused or foreground object. If no application name is available, the add-on cannot apply an application-specific rule for that focus event.
- In all-applications mode, Screen Curtain remains enabled as focus moves between applications.
- When all-applications mode is turned off with NVDA+H, the saved per-application list is cleared.
- The add-on has no separate pause or disable-automation shortcut.

## Settings and data

Focus Curtain stores its settings in a file named `focusCurtainSettings.json` in the NVDA configuration folder. The file contains the automation-enabled state, all-applications mode, and the names of selected applications. The add-on does not include network or cloud synchronisation functionality.

## Troubleshooting

- **The shortcut does not work:** Make sure NVDA is running and try the shortcut again. The shortcuts use the NVDA modifier key configured on your system (usually Insert or Caps Lock).
- **The add-on cannot identify an application:** Focus an accessible control in the target application and try NVDA+G again. The add-on relies on the application name supplied by NVDA.
- **Screen Curtain does not change:** Check the NVDA log for errors. If the add-on reports that it could not change Screen Curtain, the Screen Curtain controller may not be available or the operation may have failed.
- **Screen Curtain covers the whole display:** This is expected behaviour of NVDA's built-in Screen Curtain, not a limitation specific to Focus Curtain.

## Compatibility and testing

The supplied manifest declares NVDA 2026.1 as the minimum required version and 2026.1 as the last tested version. This package has not been executed inside NVDA as part of this documentation update. Compatibility and behaviour should be verified in the declared NVDA version before publication.

## Installation and removal

Install the `.nvda-addon` package through NVDA's Add-on Store or by opening the package and following NVDA's installation prompts. Restart NVDA if requested. To remove the add-on, open NVDA's Add-on Store, locate Focus Curtain in the installed add-ons list, and use the available remove option. Restart NVDA if requested.

## Support and feedback

For support, bug reports, or feature requests, use the project's GitHub Issues page once the repository has been created and linked in the add-on manifest.

---
