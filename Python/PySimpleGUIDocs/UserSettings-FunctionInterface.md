# User Settings API  - Function Interface
You have a couple of ways to access User Settings if your information is stored in JSON format. If you're using the INI format, then you must use the `UserSettings` object.

These are particularly useful directly in layouts, allowing you to you can easily set default values.

Returns the current settings dictionary. If you've not setup the filename for the settings, a default one will be used and then read.

```
user_settings()
```

Parameter Descriptions:

Type

Name

Meaning

(dict or str)

**RETURN**

The current settings dictionary as a dictionary or a nicely formatted string representing it

Deletes an individual entry. If no filename has been specified up to this point, then a default filename will be used. After value has been deleted, the settings file is written to disk.

```
user_settings_delete_entry(key)
```

Parameter Descriptions:

Type

Name

Meaning

Any

key

Setting to be saved. Can be any valid dictionary key type (hashable)

Deltes the filename and path for your settings file. Either paramter can be optional. If you don't choose a path, one is provided for you that is OS specific Windows path default = users/name/AppData/Local/PySimpleGUI/settings. If you don't choose a filename, your application's filename + '.json' will be used Also sets your current dictionary to a blank one.

```
user_settings_delete_filename(filename = None,
    path = None,
    report_error = False)
```

Parameter Descriptions:

Type

Name

Meaning

str

filename

The name of the file to use. Can be a full path and filename or just filename

str

path

The folder that the settings file will be stored in. Do not include the filename.

Determines if a settings file exists. If so a boolean True is returned. If either a filename or a path is not included, then the appropriate default will be used.

```
user_settings_file_exists(filename = None, path = None)
```

Parameter Descriptions:

Type

Name

Meaning

str

filename

Filename to check

str

path

Path to the file. Defaults to a specific folder depending on the operating system

(bool)

**RETURN**

True if the file exists

Sets the filename and path for your settings file. Either paramter can be optional.

If you don't choose a path, one is provided for you that is OS specific Windows path default = users/name/AppData/Local/PySimpleGUI/settings.

If you don't choose a filename, your application's filename + '.json' will be used.

Normally the filename and path are split in the user_settings calls. However for this call they can be combined so that the filename contains both the path and filename.

```
user_settings_filename(filename = None, path = None)
```

Parameter Descriptions:

Type

Name

Meaning

str

filename

The name of the file to use. Can be a full path and filename or just filename

str

path

The folder that the settings file will be stored in. Do not include the filename.

(str)

**RETURN**

The full pathname of the settings file that has both the path and filename combined.

Returns the value of a specified setting. If the setting is not found in the settings dictionary, then the user specified default value will be returned. It no default is specified and nothing is found, then None is returned. If the key isn't in the dictionary, then it will be added and the settings file saved. If no filename has been specified up to this point, then a default filename will be assigned and used. The settings are SAVED prior to returning.

```
user_settings_get_entry(key, default = None)
```

Parameter Descriptions:

Type

Name

Meaning

Any

key

Key used to lookup the setting in the settings dictionary

Any

default

Value to use should the key not be found in the dictionary

(Any)

**RETURN**

Value of specified settings

Specifies the path and filename to use for the settings and reads the contents of the file. The filename can be a full filename including a path, or the path can be specified separately. If no filename is specified, then the caller's filename will be used with the extension ".json"

```
user_settings_load(filename = None, path = None)
```

Parameter Descriptions:

Type

Name

Meaning

str

filename

Filename to load settings from (and save to in the future)

str

path

Path to the file. Defaults to a specific folder depending on the operating system

(dict)

**RETURN**

The settings dictionary (i.e. all settings)

Saves the current settings dictionary. If a filename or path is specified in the call, then it will override any previously specitfied filename to create a new settings file. The settings dictionary is then saved to the newly defined file.

```
user_settings_save(filename = None, path = None)
```

Parameter Descriptions:

Type

Name

Meaning

str

filename

The fFilename to save to. Can specify a path or just the filename. If no filename specified, then the caller's filename will be used.

str

path

The (optional) path to use to save the file.

(str)

**RETURN**

The full path and filename used to save the settings

Sets an individual setting to the specified value. If no filename has been specified up to this point, then a default filename will be used. After value has been modified, the settings file is written to disk.

```
user_settings_set_entry(key, value)
```

Parameter Descriptions:

Type

Name

Meaning

Any

key

Setting to be saved. Can be any valid dictionary key type

Any

value

Value to save as the setting's value. Can be anything

Used to control the display of error messages. By default, error messages are displayed to stdout.

```
user_settings_silent_on_error(silent_on_error = False)
```

Parameter Descriptions:

Type

Name

Meaning

bool

silent_on_error

If True then all error messages are silenced (not displayed on the console)

Writes a specified dictionary to the currently defined settings filename.

```
user_settings_write_new_dictionary(settings_dict)
```

Parameter Descriptions:

Type

Name

Meaning

dict

settings_dict

The dictionary to be written to the currently defined settings file

[Back](./_Elements)
