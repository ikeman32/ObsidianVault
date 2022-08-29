# Popup Not PEP8 Compliant
**_You should not use these function names!_**

These versions of the popup functions are here only for backwards compatibility. Instead use the popup functions that have snake_case rather than CamelCase.

Popup - Display a popup Window with as many parms as you wish to include. This is the GUI equivalent of the "print" statement. It's also great for "pausing" your program's flow until the user can read some error messages.

If this popup doesn't have the features you want, then you can easily make your own. Popups can be accomplished in 1 line of code: choice, _ = sg.Window('Continue?', [[sg.T('Do you want to continue?')], [sg.Yes(s=10), sg.No(s=10)]], disable_close=True).read(close=True)

```
Popup(args=*<1 or N object>,
    title = None,
    button_color = None,
    background_color = None,
    text_color = None,
    button_type = 0,
    auto_close = False,
    auto_close_duration = None,
    custom_text = (None, None),
    non_blocking = False,
    icon = None,
    line_width = None,
    font = None,
    no_titlebar = False,
    grab_anywhere = False,
    keep_on_top = None,
    location = (None, None),
    relative_location = (None, None),
    any_key_closes = False,
    image = None,
    modal = True)
```

Parameter Descriptions:

Type

Name

Meaning

Any

*args

Variable number of your arguments. Load up the call with stuff to see!

str

title

Optional title for the window. If none provided, the first arg will be used instead.

(str, str) or None

button_color

Color of the buttons shown (text color, button color)

str

background_color

Window's background color

str

text_color

text color

int

button_type

NOT USER SET! Determines which pre-defined buttons will be shown (Default value = POPUP_BUTTONS_OK). There are many Popup functions and they call Popup, changing this parameter to get the desired effect.

bool

auto_close

If True the window will automatically close

int

auto_close_duration

time in seconds to keep window open before closing it automatically

(str, str) or str

custom_text

A string or pair of strings that contain the text to display on the buttons

bool

non_blocking

If True then will immediately return from the function without waiting for the user's input.

str or bytes

icon

icon to display on the window. Same format as a Window call

int

line_width

Width of lines in characters. Defaults to MESSAGE_BOX_LINE_WIDTH

str or Tuple[font_name, size, modifiers]

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

no_titlebar

If True will not show the frame around the window and the titlebar across the top

bool

grab_anywhere

If True can grab anywhere to move the window. If no_titlebar is True, grab_anywhere should likely be enabled too

(int, int)

location

Location on screen to display the top left corner of window. Defaults to window centered on screen

(int, int)

relative_location

(x,y) location relative to the default location of the window, in pixels. Normally the window centers. This location is relative to the location the window would be created. Note they can be negative.

bool

keep_on_top

If True the window will remain above all current windows

bool

any_key_closes

If True then will turn on return_keyboard_events for the window which will cause window to close as soon as any key is pressed. Normally the return key only will close the window. Default is false.

str or bytes

image

Image to include at the top of the popup window

bool

modal

If True then makes the popup will behave like a Modal window... all other windows are non-operational until this one is closed. Default = True

str or None

**RETURN**

Returns text of the button that was pressed. None will be returned if user closed window with X

Show animation one frame at a time. This function has its own internal clocking meaning you can call it at any frequency and the rate the frames of video is shown remains constant. Maybe your frames update every 30 ms but your event loop is running every 10 ms. You don't have to worry about delaying, just call it every time through the loop.

```
PopupAnimated(image_source,
    message = None,
    background_color = None,
    text_color = None,
    font = None,
    no_titlebar = True,
    grab_anywhere = True,
    keep_on_top = True,
    location = (None, None),
    relative_location = (None, None),
    alpha_channel = None,
    time_between_frames = 0,
    transparent_color = None,
    title = "",
    icon = None)
```

Parameter Descriptions:

Type

Name

Meaning

str or bytes or None

image_source

Either a filename or a base64 string. Use None to close the window.

str

message

An optional message to be shown with the animation

str

background_color

color of background

str

text_color

color of the text

str or tuple

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

no_titlebar

If True then the titlebar and window frame will not be shown

bool

grab_anywhere

If True then you can move the window just clicking anywhere on window, hold and drag

bool

keep_on_top

If True then Window will remain on top of all other windows currently shownn

(int, int)

location

(x,y) location on the screen to place the top left corner of your window. Default is to center on screen

(int, int)

relative_location

(x,y) location relative to the default location of the window, in pixels. Normally the window centers. This location is relative to the location the window would be created. Note they can be negative.

float

alpha_channel

Window transparency 0 = invisible 1 = completely visible. Values between are see through

int

time_between_frames

Amount of time in milliseconds between each frame

str

transparent_color

This color will be completely see-through in your window. Can even click through

str

title

Title that will be shown on the window

str or bytes

icon

Same as Window icon parameter. Can be either a filename or Base64 byte string. For Windows if filename, it MUST be ICO format. For Linux, must NOT be ICO

bool

**RETURN**

True if the window updated OK. False if the window was closed

Display a Popup without a titlebar. Enables grab anywhere so you can move it

```
PopupAnnoying(args=*<1 or N object>,
    title = None,
    button_type = 0,
    button_color = None,
    background_color = None,
    text_color = None,
    auto_close = False,
    auto_close_duration = None,
    non_blocking = False,
    icon = None,
    line_width = None,
    font = None,
    grab_anywhere = True,
    keep_on_top = None,
    location = (None, None),
    relative_location = (None, None),
    image = None,
    modal = True)
```

Parameter Descriptions:

Type

Name

Meaning

Any

*args

Variable number of items to display

str

title

Title to display in the window.

int

button_type

Determines which pre-defined buttons will be shown (Default value = POPUP_BUTTONS_OK).

(str, str) or str

button_color

button color (foreground, background)

str

background_color

color of background

str

text_color

color of the text

bool

auto_close

if True window will close itself

int or float

auto_close_duration

Older versions only accept int. Time in seconds until window will close

bool

non_blocking

if True the call will immediately return rather than waiting on user input

bytes or str

icon

filename or base64 string to be used for the window's icon

int

line_width

Width of lines in characters

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

grab_anywhere

If True: can grab anywhere to move the window (Default = False)

bool

keep_on_top

If True the window will remain above all current windows

(int, int)

location

Location of upper left corner of the window

(int, int)

relative_location

(x,y) location relative to the default location of the window, in pixels. Normally the window centers. This location is relative to the location the window would be created. Note they can be negative.

str or bytes

image

Image to include at the top of the popup window

bool

modal

If True then makes the popup will behave like a Modal window... all other windows are non-operational until this one is closed. Default = True

str or None or TIMEOUT_KEY

**RETURN**

Returns text of the button that was pressed. None will be returned if user closed window with X

Popup that closes itself after some time period

```
PopupAutoClose(args=*<1 or N object>,
    title = None,
    button_type = 0,
    button_color = None,
    background_color = None,
    text_color = None,
    auto_close = True,
    auto_close_duration = None,
    non_blocking = False,
    icon = None,
    line_width = None,
    font = None,
    no_titlebar = False,
    grab_anywhere = False,
    keep_on_top = None,
    location = (None, None),
    relative_location = (None, None),
    image = None,
    modal = True)
```

Parameter Descriptions:

Type

Name

Meaning

Any

*args

Variable number of items to display

str

title

Title to display in the window.

int

button_type

Determines which pre-defined buttons will be shown (Default value = POPUP_BUTTONS_OK).

(str, str) or str

button_color

button color (foreground, background)

str

background_color

color of background

str

text_color

color of the text

bool

auto_close

if True window will close itself

int or float

auto_close_duration

Older versions only accept int. Time in seconds until window will close

bool

non_blocking

if True the call will immediately return rather than waiting on user input

bytes or str

icon

filename or base64 string to be used for the window's icon

int

line_width

Width of lines in characters

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

no_titlebar

If True no titlebar will be shown

bool

grab_anywhere

If True: can grab anywhere to move the window (Default = False)

bool

keep_on_top

If True the window will remain above all current windows

(int, int)

location

Location of upper left corner of the window

(int, int)

relative_location

(x,y) location relative to the default location of the window, in pixels. Normally the window centers. This location is relative to the location the window would be created. Note they can be negative.

str or bytes

image

Image to include at the top of the popup window

bool

modal

If True then makes the popup will behave like a Modal window... all other windows are non-operational until this one is closed. Default = True

str or None or TIMEOUT_KEY

**RETURN**

Returns text of the button that was pressed. None will be returned if user closed window with X

Display Popup with "cancelled" button text

```
PopupCancel(args=*<1 or N object>,
    title = None,
    button_color = None,
    background_color = None,
    text_color = None,
    auto_close = False,
    auto_close_duration = None,
    non_blocking = False,
    icon = None,
    line_width = None,
    font = None,
    no_titlebar = False,
    grab_anywhere = False,
    keep_on_top = None,
    location = (None, None),
    relative_location = (None, None),
    image = None,
    modal = True)
```

Parameter Descriptions:

Type

Name

Meaning

Any

*args

Variable number of items to display

str

title

Title to display in the window.

(str, str) or str

button_color

button color (foreground, background)

str

background_color

color of background

str

text_color

color of the text

bool

auto_close

if True window will close itself

int or float

auto_close_duration

Older versions only accept int. Time in seconds until window will close

bool

non_blocking

if True the call will immediately return rather than waiting on user input

bytes or str

icon

filename or base64 string to be used for the window's icon

int

line_width

Width of lines in characters

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

no_titlebar

If True no titlebar will be shown

bool

grab_anywhere

If True: can grab anywhere to move the window (Default = False)

bool

keep_on_top

If True the window will remain above all current windows

(int, int)

location

Location of upper left corner of the window

(int, int)

relative_location

(x,y) location relative to the default location of the window, in pixels. Normally the window centers. This location is relative to the location the window would be created. Note they can be negative.

str or bytes

image

Image to include at the top of the popup window

bool

modal

If True then makes the popup will behave like a Modal window... all other windows are non-operational until this one is closed. Default = True

str or None or TIMEOUT_KEY

**RETURN**

Returns text of the button that was pressed. None will be returned if user closed window with X

Popup with colored button and 'Error' as button text

```
PopupError(args=*<1 or N object>,
    title = None,
    button_color = (None, None),
    background_color = None,
    text_color = None,
    auto_close = False,
    auto_close_duration = None,
    non_blocking = False,
    icon = None,
    line_width = None,
    font = None,
    no_titlebar = False,
    grab_anywhere = False,
    keep_on_top = None,
    location = (None, None),
    relative_location = (None, None),
    image = None,
    modal = True)
```

Parameter Descriptions:

Type

Name

Meaning

Any

*args

Variable number of items to display

str

title

Title to display in the window.

(str, str) or str

button_color

button color (foreground, background)

str

background_color

color of background

str

text_color

color of the text

bool

auto_close

if True window will close itself

int or float

auto_close_duration

Older versions only accept int. Time in seconds until window will close

bool

non_blocking

if True the call will immediately return rather than waiting on user input

bytes or str

icon

filename or base64 string to be used for the window's icon

int

line_width

Width of lines in characters

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

no_titlebar

If True no titlebar will be shown

bool

grab_anywhere

If True: can grab anywhere to move the window (Default = False)

bool

keep_on_top

If True the window will remain above all current windows

(int, int)

location

Location of upper left corner of the window

(int, int)

relative_location

(x,y) location relative to the default location of the window, in pixels. Normally the window centers. This location is relative to the location the window would be created. Note they can be negative.

str or bytes

image

Image to include at the top of the popup window

bool

modal

If True then makes the popup will behave like a Modal window... all other windows are non-operational until this one is closed. Default = True

str or None or TIMEOUT_KEY

**RETURN**

Returns text of the button that was pressed. None will be returned if user closed window with X

Display popup window with text entry field and browse button so that a file can be chosen by user.

```
PopupGetFile(message,
    title = None,
    default_path = "",
    default_extension = "",
    save_as = False,
    multiple_files = False,
    file_types = (('ALL Files', '*.* *'),),
    no_window = False,
    size = (None, None),
    button_color = None,
    background_color = None,
    text_color = None,
    icon = None,
    font = None,
    no_titlebar = False,
    grab_anywhere = False,
    keep_on_top = None,
    location = (None, None),
    relative_location = (None, None),
    initial_folder = None,
    image = None,
    files_delimiter = ";",
    modal = True,
    history = False,
    show_hidden = True,
    history_setting_filename = None)
```

Parameter Descriptions:

Type

Name

Meaning

str

message

message displayed to user

str

title

Window title

str

default_path

path to display to user as starting point (filled into the input field)

str

default_extension

If no extension entered by user, add this to filename (only used in saveas dialogs)

bool

save_as

if True, the "save as" dialog is shown which will verify before overwriting

bool

multiple_files

if True, then allows multiple files to be selected that are returned with ';' between each filename

Tuple[Tuple[str,str]]

file_types

List of extensions to show using wildcards. All files (the default) = (("ALL Files", "_._ *"),).

bool

no_window

if True, no PySimpleGUI window will be shown. Instead just the tkinter dialog is shown

(int, int)

size

(width, height) of the InputText Element or Combo element if using history feature

(str, str) or str

button_color

Color of the button (text, background)

str

background_color

background color of the entire window

str

text_color

color of the text

bytes or str

icon

filename or base64 string to be used for the window's icon

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

no_titlebar

If True no titlebar will be shown

bool

grab_anywhere

If True: can grab anywhere to move the window (Default = False)

bool

keep_on_top

If True the window will remain above all current windows

(int, int)

location

Location of upper left corner of the window

(int, int)

relative_location

(x,y) location relative to the default location of the window, in pixels. Normally the window centers. This location is relative to the location the window would be created. Note they can be negative.

str

initial_folder

location in filesystem to begin browsing

str or bytes

image

Image to include at the top of the popup window

str

files_delimiter

String to place between files when multiple files are selected. Normally a ;

bool

modal

If True then makes the popup will behave like a Modal window... all other windows are non-operational until this one is closed. Default = True

bool

history

If True then enable a "history" feature that will display previous entries used. Uses settings filename provided or default if none provided

bool

show_hidden

If True then enables the checkbox in the system dialog to select hidden files to be shown

str

history_setting_filename

Filename to use for the User Settings. Will store list of previous entries in this settings file

str or None

**RETURN**

string representing the file(s) chosen, None if cancelled or window closed with X

Display popup with text entry field and browse button so that a folder can be chosen.

```
PopupGetFolder(message,
    title = None,
    default_path = "",
    no_window = False,
    size = (None, None),
    button_color = None,
    background_color = None,
    text_color = None,
    icon = None,
    font = None,
    no_titlebar = False,
    grab_anywhere = False,
    keep_on_top = None,
    location = (None, None),
    relative_location = (None, None),
    initial_folder = None,
    image = None,
    modal = True,
    history = False,
    history_setting_filename = None)
```

Parameter Descriptions:

Type

Name

Meaning

str

message

message displayed to user

str

title

Window title

str

default_path

path to display to user as starting point (filled into the input field)

bool

no_window

if True, no PySimpleGUI window will be shown. Instead just the tkinter dialog is shown

(int, int)

size

(width, height) of the InputText Element

(str, str) or str

button_color

button color (foreground, background)

str

background_color

color of background

str

text_color

color of the text

bytes or str

icon

filename or base64 string to be used for the window's icon

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

no_titlebar

If True no titlebar will be shown

bool

grab_anywhere

If True: can grab anywhere to move the window (Default = False)

bool

keep_on_top

If True the window will remain above all current windows

(int, int)

location

Location of upper left corner of the window

(int, int)

relative_location

(x,y) location relative to the default location of the window, in pixels. Normally the window centers. This location is relative to the location the window would be created. Note they can be negative.

str

initial_folder

location in filesystem to begin browsing

str or bytes

image

Image to include at the top of the popup window

bool

modal

If True then makes the popup will behave like a Modal window... all other windows are non-operational until this one is closed. Default = True

bool

history

If True then enable a "history" feature that will display previous entries used. Uses settings filename provided or default if none provided

str

history_setting_filename

Filename to use for the User Settings. Will store list of previous entries in this settings file

str or None

**RETURN**

string representing the path chosen, None if cancelled or window closed with X

Display Popup with text entry field. Returns the text entered or None if closed / cancelled

```
PopupGetText(message,
    title = None,
    default_text = "",
    password_char = "",
    size = (None, None),
    button_color = None,
    background_color = None,
    text_color = None,
    icon = None,
    font = None,
    no_titlebar = False,
    grab_anywhere = False,
    keep_on_top = None,
    location = (None, None),
    relative_location = (None, None),
    image = None,
    modal = True)
```

Parameter Descriptions:

Type

Name

Meaning

str

message

message displayed to user

str

title

Window title

str

default_text

default value to put into input area

str

password_char

character to be shown instead of actually typed characters

(int, int)

size

(width, height) of the InputText Element

(str, str) or str

button_color

Color of the button (text, background)

str

background_color

background color of the entire window

str

text_color

color of the message text

bytes or str

icon

filename or base64 string to be used for the window's icon

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

no_titlebar

If True no titlebar will be shown

bool

grab_anywhere

If True can click and drag anywhere in the window to move the window

bool

keep_on_top

If True the window will remain above all current windows

(int, int)

location

(x,y) Location on screen to display the upper left corner of window

(int, int)

relative_location

(x,y) location relative to the default location of the window, in pixels. Normally the window centers. This location is relative to the location the window would be created. Note they can be negative.

str or bytes

image

Image to include at the top of the popup window

bool

modal

If True then makes the popup will behave like a Modal window... all other windows are non-operational until this one is closed. Default = True

str or None

**RETURN**

Text entered or None if window was closed or cancel button clicked

Display a Popup without a titlebar. Enables grab anywhere so you can move it

```
PopupNoBorder(args=*<1 or N object>,
    title = None,
    button_type = 0,
    button_color = None,
    background_color = None,
    text_color = None,
    auto_close = False,
    auto_close_duration = None,
    non_blocking = False,
    icon = None,
    line_width = None,
    font = None,
    grab_anywhere = True,
    keep_on_top = None,
    location = (None, None),
    relative_location = (None, None),
    image = None,
    modal = True)
```

Parameter Descriptions:

Type

Name

Meaning

Any

*args

Variable number of items to display

str

title

Title to display in the window.

int

button_type

Determines which pre-defined buttons will be shown (Default value = POPUP_BUTTONS_OK).

(str, str) or str

button_color

button color (foreground, background)

str

background_color

color of background

str

text_color

color of the text

bool

auto_close

if True window will close itself

int or float

auto_close_duration

Older versions only accept int. Time in seconds until window will close

bool

non_blocking

if True the call will immediately return rather than waiting on user input

bytes or str

icon

filename or base64 string to be used for the window's icon

int

line_width

Width of lines in characters

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

grab_anywhere

If True: can grab anywhere to move the window (Default = False)

bool

keep_on_top

If True the window will remain above all current windows

(int, int)

location

Location of upper left corner of the window

(int, int)

relative_location

(x,y) location relative to the default location of the window, in pixels. Normally the window centers. This location is relative to the location the window would be created. Note they can be negative.

str or bytes

image

Image to include at the top of the popup window

bool

modal

If True then makes the popup will behave like a Modal window... all other windows are non-operational until this one is closed. Default = True

str or None or TIMEOUT_KEY

**RETURN**

Returns text of the button that was pressed. None will be returned if user closed window with X

Show a Popup but without any buttons

```
PopupNoButtons(args=*<1 or N object>,
    title = None,
    background_color = None,
    text_color = None,
    auto_close = False,
    auto_close_duration = None,
    non_blocking = False,
    icon = None,
    line_width = None,
    font = None,
    no_titlebar = False,
    grab_anywhere = False,
    keep_on_top = None,
    location = (None, None),
    relative_location = (None, None),
    image = None,
    modal = True)
```

Parameter Descriptions:

Type

Name

Meaning

Any

*args

Variable number of items to display

str

title

Title to display in the window.

str

background_color

color of background

str

text_color

color of the text

bool

auto_close

if True window will close itself

int or float

auto_close_duration

Older versions only accept int. Time in seconds until window will close

bool

non_blocking

If True then will immediately return from the function without waiting for the user's input. (Default = False)

bytes or str

icon

filename or base64 string to be used for the window's icon

int

line_width

Width of lines in characters

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

no_titlebar

If True no titlebar will be shown

bool

grab_anywhere

If True, than can grab anywhere to move the window (Default = False)

(int, int)

location

Location of upper left corner of the window

(int, int)

relative_location

(x,y) location relative to the default location of the window, in pixels. Normally the window centers. This location is relative to the location the window would be created. Note they can be negative.

str or bytes

image

Image to include at the top of the popup window

bool

modal

If True then makes the popup will behave like a Modal window... all other windows are non-operational until this one is closed. Default = True

str or None or TIMEOUT_KEY

**RETURN**

Returns text of the button that was pressed. None will be returned if user closed window with X

Display a Popup without a titlebar. Enables grab anywhere so you can move it

```
PopupNoFrame(args=*<1 or N object>,
    title = None,
    button_type = 0,
    button_color = None,
    background_color = None,
    text_color = None,
    auto_close = False,
    auto_close_duration = None,
    non_blocking = False,
    icon = None,
    line_width = None,
    font = None,
    grab_anywhere = True,
    keep_on_top = None,
    location = (None, None),
    relative_location = (None, None),
    image = None,
    modal = True)
```

Parameter Descriptions:

Type

Name

Meaning

Any

*args

Variable number of items to display

str

title

Title to display in the window.

int

button_type

Determines which pre-defined buttons will be shown (Default value = POPUP_BUTTONS_OK).

(str, str) or str

button_color

button color (foreground, background)

str

background_color

color of background

str

text_color

color of the text

bool

auto_close

if True window will close itself

int or float

auto_close_duration

Older versions only accept int. Time in seconds until window will close

bool

non_blocking

if True the call will immediately return rather than waiting on user input

bytes or str

icon

filename or base64 string to be used for the window's icon

int

line_width

Width of lines in characters

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

grab_anywhere

If True: can grab anywhere to move the window (Default = False)

bool

keep_on_top

If True the window will remain above all current windows

(int, int)

location

Location of upper left corner of the window

(int, int)

relative_location

(x,y) location relative to the default location of the window, in pixels. Normally the window centers. This location is relative to the location the window would be created. Note they can be negative.

str or bytes

image

Image to include at the top of the popup window

bool

modal

If True then makes the popup will behave like a Modal window... all other windows are non-operational until this one is closed. Default = True

str or None or TIMEOUT_KEY

**RETURN**

Returns text of the button that was pressed. None will be returned if user closed window with X

Display a Popup without a titlebar. Enables grab anywhere so you can move it

```
PopupNoTitlebar(args=*<1 or N object>,
    title = None,
    button_type = 0,
    button_color = None,
    background_color = None,
    text_color = None,
    auto_close = False,
    auto_close_duration = None,
    non_blocking = False,
    icon = None,
    line_width = None,
    font = None,
    grab_anywhere = True,
    keep_on_top = None,
    location = (None, None),
    relative_location = (None, None),
    image = None,
    modal = True)
```

Parameter Descriptions:

Type

Name

Meaning

Any

*args

Variable number of items to display

str

title

Title to display in the window.

int

button_type

Determines which pre-defined buttons will be shown (Default value = POPUP_BUTTONS_OK).

(str, str) or str

button_color

button color (foreground, background)

str

background_color

color of background

str

text_color

color of the text

bool

auto_close

if True window will close itself

int or float

auto_close_duration

Older versions only accept int. Time in seconds until window will close

bool

non_blocking

if True the call will immediately return rather than waiting on user input

bytes or str

icon

filename or base64 string to be used for the window's icon

int

line_width

Width of lines in characters

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

grab_anywhere

If True: can grab anywhere to move the window (Default = False)

bool

keep_on_top

If True the window will remain above all current windows

(int, int)

location

Location of upper left corner of the window

(int, int)

relative_location

(x,y) location relative to the default location of the window, in pixels. Normally the window centers. This location is relative to the location the window would be created. Note they can be negative.

str or bytes

image

Image to include at the top of the popup window

bool

modal

If True then makes the popup will behave like a Modal window... all other windows are non-operational until this one is closed. Default = True

str or None or TIMEOUT_KEY

**RETURN**

Returns text of the button that was pressed. None will be returned if user closed window with X

Show Popup window and immediately return (does not block)

```
PopupNonBlocking(args=*<1 or N object>,
    title = None,
    button_type = 0,
    button_color = None,
    background_color = None,
    text_color = None,
    auto_close = False,
    auto_close_duration = None,
    non_blocking = True,
    icon = None,
    line_width = None,
    font = None,
    no_titlebar = False,
    grab_anywhere = False,
    keep_on_top = None,
    location = (None, None),
    relative_location = (None, None),
    image = None,
    modal = False)
```

Parameter Descriptions:

Type

Name

Meaning

Any

*args

Variable number of items to display

str

title

Title to display in the window.

int

button_type

Determines which pre-defined buttons will be shown (Default value = POPUP_BUTTONS_OK).

(str, str) or str

button_color

button color (foreground, background)

str

background_color

color of background

str

text_color

color of the text

bool

auto_close

if True window will close itself

int or float

auto_close_duration

Older versions only accept int. Time in seconds until window will close

bool

non_blocking

if True the call will immediately return rather than waiting on user input

bytes or str

icon

filename or base64 string to be used for the window's icon

int

line_width

Width of lines in characters

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

no_titlebar

If True no titlebar will be shown

bool

grab_anywhere

If True: can grab anywhere to move the window (Default = False)

(int, int)

location

Location of upper left corner of the window

(int, int)

relative_location

(x,y) location relative to the default location of the window, in pixels. Normally the window centers. This location is relative to the location the window would be created. Note they can be negative.

str or bytes

image

Image to include at the top of the popup window

bool

modal

If True then makes the popup will behave like a Modal window... all other windows are non-operational until this one is closed. Default = False

str or None

**RETURN**

Reason for popup closing

Display Popup with OK button only

```
PopupOK(args=*<1 or N object>,
    title = None,
    button_color = None,
    background_color = None,
    text_color = None,
    auto_close = False,
    auto_close_duration = None,
    non_blocking = False,
    icon = None,
    line_width = None,
    font = None,
    no_titlebar = False,
    grab_anywhere = False,
    keep_on_top = None,
    location = (None, None),
    relative_location = (None, None),
    image = None,
    modal = True)
```

Parameter Descriptions:

Type

Name

Meaning

Any

*args

Variable number of items to display

str

title

Title to display in the window.

(str, str) or str

button_color

button color (foreground, background)

str

background_color

color of background

str

text_color

color of the text

bool

auto_close

if True window will close itself

int or float

auto_close_duration

Older versions only accept int. Time in seconds until window will close

bool

non_blocking

if True the call will immediately return rather than waiting on user input

bytes or str

icon

filename or base64 string to be used for the window's icon

int

line_width

Width of lines in characters

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

no_titlebar

If True no titlebar will be shown

bool

grab_anywhere

If True: can grab anywhere to move the window (Default = False)

bool

keep_on_top

If True the window will remain above all current windows

(int, int)

location

Location of upper left corner of the window

(int, int)

relative_location

(x,y) location relative to the default location of the window, in pixels. Normally the window centers. This location is relative to the location the window would be created. Note they can be negative.

str or bytes

image

Image to include at the top of the popup window

bool

modal

If True then makes the popup will behave like a Modal window... all other windows are non-operational until this one is closed. Default = True

str or None or TIMEOUT_KEY

**RETURN**

Returns text of the button that was pressed. None will be returned if user closed window with X

Display popup with OK and Cancel buttons

```
PopupOKCancel(args=*<1 or N object>,
    title = None,
    button_color = None,
    background_color = None,
    text_color = None,
    auto_close = False,
    auto_close_duration = None,
    non_blocking = False,
    icon = ...,
    line_width = None,
    font = None,
    no_titlebar = False,
    grab_anywhere = False,
    keep_on_top = None,
    location = (None, None),
    relative_location = (None, None),
    image = None,
    modal = True)
```

Parameter Descriptions:

Type

Name

Meaning

Any

*args

Variable number of items to display

str

title

Title to display in the window.

(str, str) or str

button_color

button color (foreground, background)

str

background_color

color of background

str

text_color

color of the text

bool

auto_close

if True window will close itself

int or float

auto_close_duration

Older versions only accept int. Time in seconds until window will close

bool

non_blocking

if True the call will immediately return rather than waiting on user input

bytes or str

icon

filename or base64 string to be used for the window's icon

int

line_width

Width of lines in characters

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

no_titlebar

If True no titlebar will be shown

bool

grab_anywhere

If True: can grab anywhere to move the window (Default = False)

bool

keep_on_top

If True the window will remain above all current windows

(int, int)

location

Location of upper left corner of the window

(int, int)

relative_location

(x,y) location relative to the default location of the window, in pixels. Normally the window centers. This location is relative to the location the window would be created. Note they can be negative.

str or bytes

image

Image to include at the top of the popup window

bool

modal

If True then makes the popup will behave like a Modal window... all other windows are non-operational until this one is closed. Default = True

"OK" or "Cancel" or None

**RETURN**

clicked button

Show Popup box that doesn't block and closes itself

```
PopupQuick(args=*<1 or N object>,
    title = None,
    button_type = 0,
    button_color = None,
    background_color = None,
    text_color = None,
    auto_close = True,
    auto_close_duration = 2,
    non_blocking = True,
    icon = None,
    line_width = None,
    font = None,
    no_titlebar = False,
    grab_anywhere = False,
    keep_on_top = None,
    location = (None, None),
    relative_location = (None, None),
    image = None,
    modal = False)
```

Parameter Descriptions:

Type

Name

Meaning

Any

*args

Variable number of items to display

str

title

Title to display in the window.

int

button_type

Determines which pre-defined buttons will be shown (Default value = POPUP_BUTTONS_OK).

(str, str) or str

button_color

button color (foreground, background)

str

background_color

color of background

str

text_color

color of the text

bool

auto_close

if True window will close itself

int or float

auto_close_duration

Older versions only accept int. Time in seconds until window will close

bool

non_blocking

if True the call will immediately return rather than waiting on user input

bytes or str

icon

filename or base64 string to be used for the window's icon

int

line_width

Width of lines in characters

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

no_titlebar

If True no titlebar will be shown

bool

grab_anywhere

If True: can grab anywhere to move the window (Default = False)

bool

keep_on_top

If True the window will remain above all current windows

(int, int)

location

Location of upper left corner of the window

(int, int)

relative_location

(x,y) location relative to the default location of the window, in pixels. Normally the window centers. This location is relative to the location the window would be created. Note they can be negative.

str or bytes

image

Image to include at the top of the popup window

bool

modal

If True then makes the popup will behave like a Modal window... all other windows are non-operational until this one is closed. Default = False

str or None or TIMEOUT_KEY

**RETURN**

Returns text of the button that was pressed. None will be returned if user closed window with X

Show Popup window with no titlebar, doesn't block, and auto closes itself.

```
PopupQuickMessage(args=*<1 or N object>,
    title = None,
    button_type = 5,
    button_color = None,
    background_color = None,
    text_color = None,
    auto_close = True,
    auto_close_duration = 2,
    non_blocking = True,
    icon = None,
    line_width = None,
    font = None,
    no_titlebar = True,
    grab_anywhere = False,
    keep_on_top = None,
    location = (None, None),
    relative_location = (None, None),
    image = None,
    modal = False)
```

Parameter Descriptions:

Type

Name

Meaning

Any

*args

Variable number of items to display

str

title

Title to display in the window.

int

button_type

Determines which pre-defined buttons will be shown (Default value = POPUP_BUTTONS_OK).

(str, str) or str

button_color

button color (foreground, background)

bool

keep_on_top

If True the window will remain above all current windows

str

background_color

color of background

str

text_color

color of the text

bool

auto_close

if True window will close itself

int or float

auto_close_duration

Older versions only accept int. Time in seconds until window will close

bool

non_blocking

if True the call will immediately return rather than waiting on user input

bytes or str

icon

filename or base64 string to be used for the window's icon

int

line_width

Width of lines in characters

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

no_titlebar

If True no titlebar will be shown

bool

grab_anywhere

If True: can grab anywhere to move the window (Default = False)

(int, int)

location

Location of upper left corner of the window

(int, int)

relative_location

(x,y) location relative to the default location of the window, in pixels. Normally the window centers. This location is relative to the location the window would be created. Note they can be negative.

str or bytes

image

Image to include at the top of the popup window

bool

modal

If True then makes the popup will behave like a Modal window... all other windows are non-operational until this one is closed. Default = False

str or None or TIMEOUT_KEY

**RETURN**

Returns text of the button that was pressed. None will be returned if user closed window with X

Show a scrolled Popup window containing the user's text that was supplied. Use with as many items to print as you want, just like a print statement.

```
PopupScrolled(args=*<1 or N object>,
    title = None,
    button_color = None,
    background_color = None,
    text_color = None,
    yes_no = False,
    no_buttons = False,
    button_justification = "l",
    auto_close = False,
    auto_close_duration = None,
    size = (None, None),
    location = (None, None),
    relative_location = (None, None),
    non_blocking = False,
    no_titlebar = False,
    grab_anywhere = False,
    keep_on_top = None,
    font = None,
    image = None,
    icon = None,
    modal = True,
    no_sizegrip = False)
```

Parameter Descriptions:

Type

Name

Meaning

Any

*args

Variable number of items to display

str

title

Title to display in the window.

(str, str) or str

button_color

button color (foreground, background)

bool

yes_no

If True, displays Yes and No buttons instead of Ok

bool

no_buttons

If True, no buttons will be shown. User will have to close using the "X"

str

button_justification

How buttons should be arranged. l, c, r for Left, Center or Right justified

bool

auto_close

if True window will close itself

int or float

auto_close_duration

Older versions only accept int. Time in seconds until window will close

(int, int)

size

(w,h) w=characters-wide, h=rows-high

(int, int)

location

Location on the screen to place the upper left corner of the window

(int, int)

relative_location

(x,y) location relative to the default location of the window, in pixels. Normally the window centers. This location is relative to the location the window would be created. Note they can be negative.

bool

non_blocking

if True the call will immediately return rather than waiting on user input

str

background_color

color of background

str

text_color

color of the text

bool

no_titlebar

If True no titlebar will be shown

bool

grab_anywhere

If True, than can grab anywhere to move the window (Default = False)

bool

keep_on_top

If True the window will remain above all current windows

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

str or bytes

image

Image to include at the top of the popup window

bytes or str

icon

filename or base64 string to be used for the window's icon

bool

modal

If True then makes the popup will behave like a Modal window... all other windows are non-operational until this one is closed. Default = True

bool

no_sizegrip

If True no Sizegrip will be shown when there is no titlebar. It's only shown if there is no titlebar

str or None or TIMEOUT_KEY

**RETURN**

Returns text of the button that was pressed. None will be returned if user closed window with X

Popup that closes itself after some time period

```
PopupTimed(args=*<1 or N object>,
    title = None,
    button_type = 0,
    button_color = None,
    background_color = None,
    text_color = None,
    auto_close = True,
    auto_close_duration = None,
    non_blocking = False,
    icon = None,
    line_width = None,
    font = None,
    no_titlebar = False,
    grab_anywhere = False,
    keep_on_top = None,
    location = (None, None),
    relative_location = (None, None),
    image = None,
    modal = True)
```

Parameter Descriptions:

Type

Name

Meaning

Any

*args

Variable number of items to display

str

title

Title to display in the window.

int

button_type

Determines which pre-defined buttons will be shown (Default value = POPUP_BUTTONS_OK).

(str, str) or str

button_color

button color (foreground, background)

str

background_color

color of background

str

text_color

color of the text

bool

auto_close

if True window will close itself

int or float

auto_close_duration

Older versions only accept int. Time in seconds until window will close

bool

non_blocking

if True the call will immediately return rather than waiting on user input

bytes or str

icon

filename or base64 string to be used for the window's icon

int

line_width

Width of lines in characters

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

no_titlebar

If True no titlebar will be shown

bool

grab_anywhere

If True: can grab anywhere to move the window (Default = False)

bool

keep_on_top

If True the window will remain above all current windows

(int, int)

location

Location of upper left corner of the window

(int, int)

relative_location

(x,y) location relative to the default location of the window, in pixels. Normally the window centers. This location is relative to the location the window would be created. Note they can be negative.

str or bytes

image

Image to include at the top of the popup window

bool

modal

If True then makes the popup will behave like a Modal window... all other windows are non-operational until this one is closed. Default = True

str or None or TIMEOUT_KEY

**RETURN**

Returns text of the button that was pressed. None will be returned if user closed window with X

Display Popup with Yes and No buttons

```
PopupYesNo(args=*<1 or N object>,
    title = None,
    button_color = None,
    background_color = None,
    text_color = None,
    auto_close = False,
    auto_close_duration = None,
    non_blocking = False,
    icon = None,
    line_width = None,
    font = None,
    no_titlebar = False,
    grab_anywhere = False,
    keep_on_top = None,
    location = (None, None),
    relative_location = (None, None),
    image = None,
    modal = True)
```

Parameter Descriptions:

Type

Name

Meaning

Any

*args

Variable number of items to display

str

title

Title to display in the window.

(str, str) or str

button_color

button color (foreground, background)

str

background_color

color of background

str

text_color

color of the text

bool

auto_close

if True window will close itself

int or float

auto_close_duration

Older versions only accept int. Time in seconds until window will close

bool

non_blocking

if True the call will immediately return rather than waiting on user input

bytes or str

icon

filename or base64 string to be used for the window's icon

int

line_width

Width of lines in characters

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

no_titlebar

If True no titlebar will be shown

bool

grab_anywhere

If True: can grab anywhere to move the window (Default = False)

bool

keep_on_top

If True the window will remain above all current windows

(int, int)

location

Location of upper left corner of the window

(int, int)

relative_location

(x,y) location relative to the default location of the window, in pixels. Normally the window centers. This location is relative to the location the window would be created. Note they can be negative.

str or bytes

image

Image to include at the top of the popup window

bool

modal

If True then makes the popup will behave like a Modal window... all other windows are non-operational until this one is closed. Default = True

"Yes" or "No" or None

**RETURN**

clicked button

[Back](./_Elements)
