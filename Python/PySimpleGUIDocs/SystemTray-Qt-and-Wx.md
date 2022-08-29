# System Tray  - Only for Qt and Wx ports. Use `psgtray` package for the tkinter port
```
A "Simulated System Tray" that duplicates the API calls available to PySimpleGUIWx and PySimpleGUIQt users.

All of the functionality works. The icon is displayed ABOVE the system tray rather than inside of it.
```

SystemTray - create an icon in the system tray

```
SystemTray(menu = None,
    filename = None,
    data = None,
    data_base64 = None,
    tooltip = None,
    metadata = None)
```

Parameter Descriptions:

Type

Name

Meaning

List[List[List[str] or str]]

menu

Menu definition. Example - ['UNUSED', ['My', 'Simple', '---', 'Menu', 'Exit']]

str

filename

filename for icon

bytes

data

in-ram image for icon (same as data_base64 parm)

bytes

data_base64

base-64 data for icon

str

tooltip

tooltip string

Any

metadata

User metadata that can be set to ANYTHING

### close

Close the system tray window

```python
close()
```

### hide

Hides the icon

```python
hide()
```

### metadata

#### property: metadata

Metadata is an SystemTray property that you can use at any time to hold any value

Type

Name

Meaning

(Any)

**return**

the current metadata value

### notify

Displays a "notification window", usually in the bottom right corner of your display. Has an icon, a title, and a message The window will slowly fade in and out if desired. Clicking on the window will cause it to move through the end the current "phase". For example, if the window was fading in and it was clicked, then it would immediately stop fading in and instead be fully visible. It's a way for the user to quickly dismiss the window.

```
notify(title,
    message,
    icon = ...,
    display_duration_in_ms = 3000,
    fade_in_duration = 1000,
    alpha = 0.9,
    location = None)
```

Parameter Descriptions:

Type

Name

Meaning

str

title

Text to be shown at the top of the window in a larger font

str

message

Text message that makes up the majority of the window

bytes or str

icon

A base64 encoded PNG/GIF image or PNG/GIF filename that will be displayed in the window

int

display_duration_in_ms

Number of milliseconds to show the window

int

fade_in_duration

Number of milliseconds to fade window in and out

float

alpha

Alpha channel. 0 - invisible 1 - fully visible

(int, int)

location

Location on the screen to display the window

(int)

**RETURN**

(int) reason for returning

### read

Reads the context menu

```
read(timeout = None)
```

Parameter Descriptions:

Type

Name

Meaning

timeout

Optional. Any value other than None indicates a non-blocking read

### show_message

Shows a balloon above icon in system tray

```
show_message(title,
    message,
    filename = None,
    data = None,
    data_base64 = None,
    messageicon = None,
    time = (1000, 3000))
```

Parameter Descriptions:

Type

Name

Meaning

str

title

Title shown in balloon

str

message

Message to be displayed

str

filename

Optional icon filename

b''

data

Optional in-ram icon

b''

data_base64

Optional base64 icon

int or (int, int)

time

Amount of time to display message in milliseconds. If tuple, first item is fade in/out duration

Any

**RETURN**

The event that happened during the display such as user clicked on message

### un_hide

Restores a previously hidden icon

```python
un_hide()
```

### update

Updates the menu, tooltip or icon

```
update(menu = None,
    tooltip = None,
    filename = None,
    data = None,
    data_base64 = None)
```

Parameter Descriptions:

Type

Name

Meaning

???

menu

menu defintion

???

tooltip

string representing tooltip

???

filename

icon filename

???

data

icon raw image

???

data_base64

icon base 64 image

---

### These are non-PEP8 Compliant Methods - do NOT use

The following methods are here for backwards compatibility reference. You will find there are PEP8 versions for each of these methods. The PEP8 versions will be all lower case and have underscores.

### Close

Close the system tray window

```python
Close()
```

### Hide

Hides the icon

```python
Hide()
```

### Read

Reads the context menu

```
Read(timeout = None)
```

Parameter Descriptions:

Type

Name

Meaning

timeout

Optional. Any value other than None indicates a non-blocking read

### ShowMessage

Shows a balloon above icon in system tray

```
ShowMessage(title,
    message,
    filename = None,
    data = None,
    data_base64 = None,
    messageicon = None,
    time = (1000, 3000))
```

Parameter Descriptions:

Type

Name

Meaning

str

title

Title shown in balloon

str

message

Message to be displayed

str

filename

Optional icon filename

b''

data

Optional in-ram icon

b''

data_base64

Optional base64 icon

int or (int, int)

time

Amount of time to display message in milliseconds. If tuple, first item is fade in/out duration

Any

**RETURN**

The event that happened during the display such as user clicked on message

### UnHide

Restores a previously hidden icon

```python
UnHide()
```

### Update

Updates the menu, tooltip or icon

```
Update(menu = None,
    tooltip = None,
    filename = None,
    data = None,
    data_base64 = None)
```

Parameter Descriptions:

Type

Name

Meaning

???

menu

menu defintion

???

tooltip

string representing tooltip

???

filename

icon filename

???

data

icon raw image

???

data_base64

icon base 64 image

[Back](./_Elements)
