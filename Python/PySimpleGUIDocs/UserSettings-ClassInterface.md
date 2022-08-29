# User Settings API -  Class Interface
he User Settings API is used to store your settings information from one session to another or from one program to another. They are stored on disk in either JSON or INI file formats.

In addition to user settings files, there is also a global PySimpleGUI settings file that PySimpleGUI uses to store information about the default Python interpreter you want to use with the Exec APIs, the default theme. You can directly access the global settings through the UserSettings object: `pysimplegui_user_settings`

User Settings

```
UserSettings(filename = None,
    path = None,
    silent_on_error = False,
    autosave = True,
    use_config_file = None,
    convert_bools_and_none = True)
```

Parameter Descriptions:

Type

Name

Meaning

(str or None)

filename

The name of the file to use. Can be a full path and filename or just filename

(str or None)

path

The folder that the settings file will be stored in. Do not include the filename.

bool

silent_on_error

If True errors will not be reported

bool

autosave

If True the settings file is saved after every update

bool

use_config_file

If True then the file format will be a config.ini rather than json

bool

convert_bools_and_none

If True then "True", "False", "None" will be converted to the Python values True, False, None when using INI files. Default is TRUE

### delete_entry

Deletes an individual entry. If no filename has been specified up to this point, then a default filename will be used. After value has been deleted, the settings file is written to disk.

```
delete_entry(key, section = None)
```

Parameter Descriptions:

Type

Name

Meaning

Any

key

Setting to be deleted. Can be any valid dictionary key type (i.e. must be hashable)

### delete_file

Deltes the filename and path for your settings file. Either paramter can be optional. If you don't choose a path, one is provided for you that is OS specific Windows path default = users/name/AppData/Local/PySimpleGUI/settings. If you don't choose a filename, your application's filename + '.json' will be used Also sets your current dictionary to a blank one.

```
delete_file(filename = None,
    path = None,
    report_error = False)
```

Parameter Descriptions:

Type

Name

Meaning

(str or None)

filename

The name of the file to use. Can be a full path and filename or just filename

(str or None)

path

The folder that the settings file will be stored in. Do not include the filename.

bool

report_error

Determines if an error should be shown if a delete error happen (i.e. file isn't present)

### delete_section

Deletes a section with the name provided in the section parameter. Your INI file will be saved afterwards if auto-save enabled (default is ON)

```
delete_section(section)
```

Parameter Descriptions:

Type

Name

Meaning

str

section

Name of the section to delete

### exists

Check if a particular settings file exists. Returns True if file exists

```
exists(filename = None, path = None)
```

Parameter Descriptions:

Type

Name

Meaning

(str or None)

filename

The name of the file to use. Can be a full path and filename or just filename

(str or None)

path

The folder that the settings file will be stored in. Do not include the filename.

### get

Returns the value of a specified setting. If the setting is not found in the settings dictionary, then the user specified default value will be returned. It no default is specified and nothing is found, then the "default value" is returned. This default can be specified in this call, or previously defined by calling set_default. If nothing specified now or previously, then None is returned as default.

```
get(key, default = None)
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

### get_dict

Returns the current settings dictionary. If you've not setup the filename for the settings, a default one will be used and then read.

Note that you can display the dictionary in text format by printing the object itself.

`get_dict()`

Type

Name

Meaning

Dict

**return**

The current settings dictionary

### get_filename

Sets the filename and path for your settings file. Either paramter can be optional.

If you don't choose a path, one is provided for you that is OS specific Windows path default = users/name/AppData/Local/PySimpleGUI/settings.

If you don't choose a filename, your application's filename + '.json' will be used.

Normally the filename and path are split in the user_settings calls. However for this call they can be combined so that the filename contains both the path and filename.

```
get_filename(filename = None, path = None)
```

Parameter Descriptions:

Type

Name

Meaning

(str or None)

filename

The name of the file to use. Can be a full path and filename or just filename

(str or None)

path

The folder that the settings file will be stored in. Do not include the filename.

(str)

**RETURN**

The full pathname of the settings file that has both the path and filename combined.

### load

Specifies the path and filename to use for the settings and reads the contents of the file. The filename can be a full filename including a path, or the path can be specified separately. If no filename is specified, then the caller's filename will be used with the extension ".json"

```
load(filename = None, path = None)
```

Parameter Descriptions:

Type

Name

Meaning

(str or None)

filename

Filename to load settings from (and save to in the future)

(str or None)

path

Path to the file. Defaults to a specific folder depending on the operating system

(dict)

**RETURN**

The settings dictionary (i.e. all settings)

### read

Reads settings file and returns the dictionary. If you have anything changed in an existing settings dictionary, you will lose your changes.

`read()`

Type

Name

Meaning

(dict)

**return**

settings dictionary

### save

Saves the current settings dictionary. If a filename or path is specified in the call, then it will override any previously specitfied filename to create a new settings file. The settings dictionary is then saved to the newly defined file.

```
save(filename = None, path = None)
```

Parameter Descriptions:

Type

Name

Meaning

(str or None)

filename

The fFilename to save to. Can specify a path or just the filename. If no filename specified, then the caller's filename will be used.

(str or None)

path

The (optional) path to use to save the file.

(str)

**RETURN**

The full path and filename used to save the settings

### set

Sets an individual setting to the specified value. If no filename has been specified up to this point, then a default filename will be used. After value has been modified, the settings file is written to disk. Note that this call is not value for a config file normally. If it is, then the key is assumed to be the Section key and the value written will be the default value.

```
set(key, value)
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

(Any)

**RETURN**

value that key was set to

### set_default_value

Set the value that will be returned if a requested setting is not found

```
set_default_value(default)
```

Parameter Descriptions:

Type

Name

Meaning

Any

default

value to be returned if a setting is not found in the settings dictionary

### set_location

Sets the location of the settings file

```
set_location(filename = None, path = None)
```

Parameter Descriptions:

Type

Name

Meaning

(str or None)

filename

The name of the file to use. Can be a full path and filename or just filename

(str or None)

path

The folder that the settings file will be stored in. Do not include the filename.

### write_new_dictionary

Writes a specified dictionary to the currently defined settings filename.

```
write_new_dictionary(settings_dict)
```

Parameter Descriptions:

Type

Name

Meaning

dict

settings_dict

The dictionary to be written to the currently defined settings file

[Back](./_Elements)
