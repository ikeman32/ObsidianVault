# Main PySimpleGUI Program  - Test Harness, Global Settings, Debug Information, Upgrade from GitHub
A convention that PySimpleGUI uses is that standalone entry points start with "main_". These calls are essentially a mini-program within the PySimpleGUI.py file.

Used to get SDK help, test the installation, get information about the versions, upgrade from GitHub.

You can call main() from your code and then access these other features such as the global settings. You can also directly call these functions.

You can also type `psgmain` from the command line to access it if you have pip installed your copy of PySimpleGUI.

The PySimpleGUI "Test Harness". This is meant to be a super-quick test of the Elements.

```
main()
```

Collect up and display the data needed to file GitHub issues. This function will place the information on the clipboard. You MUST paste the information from the clipboard prior to existing your application (except on Windows).

```
main_get_debug_data(suppress_popup = False)
```

Parameter Descriptions:

Type

Name

Meaning

bool

suppress_popup

If True no popup window will be shown. The string will be only returned, not displayed

Window to set settings that will be used across all PySimpleGUI programs that choose to use them. Use set_options to set the path to the folder for all PySimpleGUI settings.

```
main_global_pysimplegui_settings()
```

Parameter Descriptions:

Type

Name

Meaning

(bool)

**RETURN**

True if settings were changed

Display a window that will display the docstrings for each PySimpleGUI Element and the Window object

```
main_sdk_help()
```

The PySimpleGUI "Test Harness". This is meant to be a super-quick test of the Elements.

```
test()
```

[Back](./_Elements)
