# Pre-Defined Buttons
Button that will show a calendar chooser window. Fills in the target element with result

```
CalendarButton(button_text,
    target = (555666777, -1),
    close_when_date_chosen = True,
    default_date_m_d_y = (None, None, None),
    image_filename = None,
    image_data = None,
    image_size = (None, None),
    image_subsample = None,
    tooltip = None,
    border_width = None,
    size = (None, None),
    s = (None, None),
    auto_size_button = None,
    button_color = None,
    disabled = False,
    font = None,
    bind_return_key = False,
    focus = False,
    pad = None,
    p = None,
    enable_events = None,
    key = None,
    k = None,
    visible = True,
    locale = None,
    format = "%Y-%m-%d %H:%M:%S",
    begin_at_sunday_plus = 0,
    month_names = None,
    day_abbreviations = None,
    title = "Choose Date",
    no_titlebar = True,
    location = (None, None),
    metadata = None,
    expand_x = False,
    expand_y = False)
```

Parameter Descriptions:

Type

Name

Meaning

str

button_text

text in the button

(int, int) or Any

target

Key or "coordinate" (see docs) of target element

bool

close_when_date_chosen

(Default = True)

(int, int or None, int)

default_date_m_d_y

Beginning date to show

image filename if there is a button image

image_filename

image filename if there is a button image

in-RAM image to be displayed on button

image_data

in-RAM image to be displayed on button

(Default = (None))

image_size

image size (O.K.)

amount to reduce the size of the image

image_subsample

amount to reduce the size of the image

str

tooltip

text, that will appear when mouse hovers over the element

width of border around element

border_width

width of border around element

(int, int)

size

(w,h) w=characters-wide, h=rows-high

(int, int) or (None, None) or int

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

bool

auto_size_button

True if button size is determined by button text

(str, str) or str

button_color

button color (foreground, background)

bool

disabled

set disable state for element (Default = False)

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

bind_return_key

(Default = False) If True, then the return key will cause a the Listbox to generate an event

bool

focus

if focus should be set to this

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

str or int or tuple or object

key

key for uniquely identify this element (for window.find_element)

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

str

locale

defines the locale used to get day names

str

format

formats result using this strftime format

List[str]

month_names

optional list of month names to use (should be 12 items)

List[str]

day_abbreviations

optional list of abbreviations to display as the day of week

str

title

Title shown on the date chooser window

bool

no_titlebar

if True no titlebar will be shown on the date chooser window

(int, int)

location

Location on the screen (x,y) to show the calendar popup window

bool

visible

set initial visibility state of the Button

Any

metadata

Anything you want to store along with this button

bool

expand_x

If True Element will expand in the Horizontal directions

bool

expand_y

If True Element will expand in the Vertical directions

(Button)

**RETURN**

returns a button

```
Cancel(button_text = "Cancel",
    size = (None, None),
    s = (None, None),
    auto_size_button = None,
    button_color = None,
    disabled = False,
    tooltip = None,
    font = None,
    bind_return_key = False,
    focus = False,
    pad = None,
    p = None,
    key = None,
    k = None,
    visible = True,
    metadata = None,
    expand_x = False,
    expand_y = False)
```

Parameter Descriptions:

Type

Name

Meaning

str

button_text

text in the button (Default value = 'Cancel')

(int, int)

size

(w,h) w=characters-wide, h=rows-high

(int, int) or (None, None) or int

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

bool

auto_size_button

True if button size is determined by button text

(str, str) or str

button_color

button color (foreground, background)

bool

disabled

set disable state for element (Default = False)

str

tooltip

text, that will appear when mouse hovers over the element

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

bind_return_key

(Default = False) If True, then the return key will cause a the Listbox to generate an event

focus

if focus should be set to this

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

str or int or tuple or object

key

key for uniquely identify this element (for window.find_element)

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

bool

visible

set initial visibility state of the Button

Any

metadata

Anything you want to store along with this button

bool

expand_x

If True Element will expand in the Horizontal directions

bool

expand_y

If True Element will expand in the Vertical directions

(Button)

**RETURN**

returns a button

```
ColorChooserButton(button_text,
    target = (555666777, -1),
    image_filename = None,
    image_data = None,
    image_size = (None, None),
    image_subsample = None,
    tooltip = None,
    border_width = None,
    size = (None, None),
    s = (None, None),
    auto_size_button = None,
    button_color = None,
    disabled = False,
    font = None,
    bind_return_key = False,
    focus = False,
    pad = None,
    p = None,
    key = None,
    k = None,
    default_color = None,
    visible = True,
    metadata = None,
    expand_x = False,
    expand_y = False)
```

Parameter Descriptions:

Type

Name

Meaning

str

button_text

text in the button

str or (int, int)

target

key or (row,col) target for the button. Note that -1 for column means 1 element to the left of this one. The constant ThisRow is used to indicate the current row. The Button itself is a valid target for some types of button

str

image_filename

image filename if there is a button image. GIFs and PNGs only.

bytes or str

image_data

Raw or Base64 representation of the image to put on button. Choose either filename or data

(int, int)

image_size

Size of the image in pixels (width, height)

int

image_subsample

amount to reduce the size of the image. Divides the size by this number. 2=1/2, 3=1/3, 4=1/4, etc

str

tooltip

text, that will appear when mouse hovers over the element

int

border_width

width of border around element

(int, int)

size

(w,h) w=characters-wide, h=rows-high

(int, int) or (None, None) or int

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

bool

auto_size_button

True if button size is determined by button text

(str, str) or str

button_color

button color (foreground, background)

bool

disabled

set disable state for element (Default = False)

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

bind_return_key

If True, then the return key will cause a the Listbox to generate an event

bool

focus

Determines if initial focus should go to this element.

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

str or int or tuple or object

key

key for uniquely identify this element (for window.find_element)

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

str

default_color

Color to be sent to tkinter to use as the default color

bool

visible

set initial visibility state of the Button

Any

metadata

User metadata that can be set to ANYTHING

bool

expand_x

If True Element will expand in the Horizontal directions

bool

expand_y

If True Element will expand in the Vertical directions

(Button)

**RETURN**

returns a button

This Button has been changed in how it works!! Your button has been replaced with a normal button that has the PySimpleGUI Debugger buggon logo on it. In your event loop, you will need to check for the event of this button and then call: show_debugger_popout_window()

```
Debug(button_text = "",
    size = (None, None),
    s = (None, None),
    auto_size_button = None,
    button_color = None,
    disabled = False,
    font = None,
    tooltip = None,
    bind_return_key = False,
    focus = False,
    pad = None,
    p = None,
    key = None,
    k = None,
    visible = True,
    metadata = None,
    expand_x = False,
    expand_y = False)
```

Parameter Descriptions:

Type

Name

Meaning

str

button_text

text in the button (Default value = '')

(int, int)

size

(w,h) w=characters-wide, h=rows-high

(int, int) or (None, None) or int

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

bool

auto_size_button

True if button size is determined by button text

(str, str) or str

button_color

button color (foreground, background)

bool

disabled

set disable state for element (Default = False)

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

str

tooltip

text, that will appear when mouse hovers over the element

bool

bind_return_key

(Default = False) If True, then the return key will cause a the Listbox to generate an event

focus

if focus should be set to this

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

str or int or tuple or object

key

key for uniquely identify this element (for window.find_element)

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

bool

visible

set initial visibility state of the Button

Any

metadata

Anything you want to store along with this button

bool

expand_x

If True Element will expand in the Horizontal directions

bool

expand_y

If True Element will expand in the Vertical directions

(Button)

**RETURN**

returns a button

This is a special type of Button.

It will close the window but NOT send an event that the window has been closed.

It's used in conjunction with non-blocking windows to silently close them. They are used to implement the non-blocking popup windows. They're also found in some Demo Programs, so look there for proper use.

```
DummyButton(button_text,
    image_filename = None,
    image_data = None,
    image_size = (None, None),
    image_subsample = None,
    border_width = None,
    tooltip = None,
    size = (None, None),
    s = (None, None),
    auto_size_button = None,
    button_color = None,
    font = None,
    disabled = False,
    bind_return_key = False,
    focus = False,
    pad = None,
    p = None,
    key = None,
    k = None,
    visible = True,
    metadata = None,
    expand_x = False,
    expand_y = False)
```

Parameter Descriptions:

Type

Name

Meaning

str

button_text

text in the button

image filename if there is a button image

image_filename

image filename if there is a button image

in-RAM image to be displayed on button

image_data

in-RAM image to be displayed on button

(Default = (None))

image_size

image size (O.K.)

amount to reduce the size of the image

image_subsample

amount to reduce the size of the image

int

border_width

width of border around element

str

tooltip

text, that will appear when mouse hovers over the element

(int, int)

size

(w,h) w=characters-wide, h=rows-high

(int, int) or (None, None) or int

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

bool

auto_size_button

True if button size is determined by button text

(str, str) or str

button_color

button color (foreground, background)

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

disabled

set disable state for element (Default = False)

bool

bind_return_key

(Default = False) If True, then the return key will cause a the Listbox to generate an event

bool

focus

if focus should be set to this

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

str or int or tuple or object

key

key for uniquely identify this element (for window.find_element)

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

bool

visible

set initial visibility state of the Button

Any

metadata

Anything you want to store along with this button

bool

expand_x

If True Element will expand in the Horizontal directions

bool

expand_y

If True Element will expand in the Vertical directions

(Button)

**RETURN**

returns a button

```
Exit(button_text = "Exit",
    size = (None, None),
    s = (None, None),
    auto_size_button = None,
    button_color = None,
    disabled = False,
    tooltip = None,
    font = None,
    bind_return_key = False,
    focus = False,
    pad = None,
    p = None,
    key = None,
    k = None,
    visible = True,
    metadata = None,
    expand_x = False,
    expand_y = False)
```

Parameter Descriptions:

Type

Name

Meaning

str

button_text

text in the button (Default value = 'Exit')

(int, int)

size

(w,h) w=characters-wide, h=rows-high

(int, int) or (None, None) or int

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

bool

auto_size_button

True if button size is determined by button text

(str, str) or str

button_color

button color (foreground, background)

bool

disabled

set disable state for element (Default = False)

str

tooltip

text, that will appear when mouse hovers over the element

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

bind_return_key

(Default = False) If True, then the return key will cause a the Listbox to generate an event

focus

if focus should be set to this

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

str or int or tuple or object

key

key for uniquely identify this element (for window.find_element)

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

bool

visible

set initial visibility state of the Button

Any

metadata

Anything you want to store along with this button

bool

expand_x

If True Element will expand in the Horizontal directions

bool

expand_y

If True Element will expand in the Vertical directions

(Button)

**RETURN**

returns a button

```
FileBrowse(button_text = "Browse",
    target = (555666777, -1),
    file_types = (('ALL Files', '*.* *'),),
    initial_folder = None,
    tooltip = None,
    size = (None, None),
    s = (None, None),
    auto_size_button = None,
    button_color = None,
    change_submits = False,
    enable_events = False,
    font = None,
    disabled = False,
    pad = None,
    p = None,
    key = None,
    k = None,
    visible = True,
    metadata = None,
    expand_x = False,
    expand_y = False)
```

Parameter Descriptions:

Type

Name

Meaning

str

button_text

text in the button (Default value = 'Browse')

str or (int, int)

target

key or (row,col) target for the button (Default value = (ThisRow, -1))

Tuple[(str, str), ...]

file_types

filter file types Default value = (("ALL Files", "_._ *"),).

initial_folder

starting path for folders and files

str

tooltip

text, that will appear when mouse hovers over the element

(int, int)

size

(w,h) w=characters-wide, h=rows-high

(int, int) or (None, None) or int

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

bool

auto_size_button

True if button size is determined by button text

(str, str) or str

button_color

button color (foreground, background)

bool

change_submits

If True, pressing Enter key submits window (Default = False)

bool

enable_events

Turns on the element specific events.(Default = False)

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

disabled

set disable state for element (Default = False)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

str or int or tuple or object

key

key for uniquely identify this element (for window.find_element)

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

bool

visible

set initial visibility state of the Button

Any

metadata

Anything you want to store along with this button

bool

expand_x

If True Element will expand in the Horizontal directions

bool

expand_y

If True Element will expand in the Vertical directions

(Button)

**RETURN**

returns a button

```
FileSaveAs(button_text = "Save As...",
    target = (555666777, -1),
    file_types = (('ALL Files', '*.* *'),),
    initial_folder = None,
    default_extension = "",
    disabled = False,
    tooltip = None,
    size = (None, None),
    s = (None, None),
    auto_size_button = None,
    button_color = None,
    change_submits = False,
    enable_events = False,
    font = None,
    pad = None,
    p = None,
    key = None,
    k = None,
    visible = True,
    metadata = None,
    expand_x = False,
    expand_y = False)
```

Parameter Descriptions:

Type

Name

Meaning

str

button_text

text in the button (Default value = 'Save As...')

str or (int, int)

target

key or (row,col) target for the button (Default value = (ThisRow, -1))

Tuple[(str, str), ...]

file_types

Default value = (("ALL Files", "_._ *"),).

str

default_extension

If no extension entered by user, add this to filename (only used in saveas dialogs)

str

initial_folder

starting path for folders and files

bool

disabled

set disable state for element (Default = False)

str

tooltip

text, that will appear when mouse hovers over the element

(int, int)

size

(w,h) w=characters-wide, h=rows-high

(int, int) or (None, None) or int

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

bool

auto_size_button

True if button size is determined by button text

(str, str) or str

button_color

button color (foreground, background)

bool

change_submits

If True, pressing Enter key submits window (Default = False)

bool

enable_events

Turns on the element specific events.(Default = False)

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

str or int or tuple or object

key

key for uniquely identify this element (for window.find_element)

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

bool

visible

set initial visibility state of the Button

Any

metadata

Anything you want to store along with this button

bool

expand_x

If True Element will expand in the Horizontal directions

bool) :return: returns a button

expand_y

If True Element will expand in the Vertical directions

(Button)

**RETURN**

returns a button

Allows browsing of multiple files. File list is returned as a single list with the delimiter defined using the files_delimiter parameter.

```
FilesBrowse(button_text = "Browse",
    target = (555666777, -1),
    file_types = (('ALL Files', '*.* *'),),
    disabled = False,
    initial_folder = None,
    tooltip = None,
    size = (None, None),
    s = (None, None),
    auto_size_button = None,
    button_color = None,
    change_submits = False,
    enable_events = False,
    font = None,
    pad = None,
    p = None,
    key = None,
    k = None,
    visible = True,
    files_delimiter = ";",
    metadata = None,
    expand_x = False,
    expand_y = False)
```

Parameter Descriptions:

Type

Name

Meaning

str

button_text

text in the button (Default value = 'Browse')

str or (int, int)

target

key or (row,col) target for the button (Default value = (ThisRow, -1))

Tuple[(str, str), ...]

file_types

Default value = (("ALL Files", "_._ *"),).

bool

disabled

set disable state for element (Default = False)

str

initial_folder

starting path for folders and files

str

tooltip

text, that will appear when mouse hovers over the element

(int, int)

size

(w,h) w=characters-wide, h=rows-high

(int, int) or (None, None) or int

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

bool

auto_size_button

True if button size is determined by button text

(str, str) or str

button_color

button color (foreground, background)

bool

change_submits

If True, pressing Enter key submits window (Default = False)

bool

enable_events

Turns on the element specific events.(Default = False)

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

str or int or tuple or object

key

key for uniquely identify this element (for window.find_element)

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

bool

visible

set initial visibility state of the Button

str

files_delimiter

String to place between files when multiple files are selected. Normally a ;

Any

metadata

Anything you want to store along with this button

bool

expand_x

If True Element will expand in the Horizontal directions

bool

expand_y

If True Element will expand in the Vertical directions

(Button)

**RETURN**

returns a button

```
FolderBrowse(button_text = "Browse",
    target = (555666777, -1),
    initial_folder = None,
    tooltip = None,
    size = (None, None),
    s = (None, None),
    auto_size_button = None,
    button_color = None,
    disabled = False,
    change_submits = False,
    enable_events = False,
    font = None,
    pad = None,
    p = None,
    key = None,
    k = None,
    visible = True,
    metadata = None,
    expand_x = False,
    expand_y = False)
```

Parameter Descriptions:

Type

Name

Meaning

str

button_text

text in the button (Default value = 'Browse')

str or (int, int)

target

target for the button (Default value = (ThisRow, -1))

str

initial_folder

starting path for folders and files

str

tooltip

text, that will appear when mouse hovers over the element

(int, int)

size

(w,h) w=characters-wide, h=rows-high

(int, int) or (None, None) or int

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

bool

auto_size_button

True if button size is determined by button text

button_color

button color (foreground, background)

bool

disabled

set disable state for element (Default = False)

bool

change_submits

If True, pressing Enter key submits window (Default = False)

bool

enable_events

Turns on the element specific events.(Default = False)

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

str or int or tuple or object

key

Used with window.find_element and with return values to uniquely identify this element

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

bool

visible

set initial visibility state of the Button

Any

metadata

Anything you want to store along with this button

bool

expand_x

If True Element will expand in the Horizontal directions

bool

expand_y

If True Element will expand in the Vertical directions

(Button)

**RETURN**

The Button created

```
Help(button_text = "Help",
    size = (None, None),
    s = (None, None),
    auto_size_button = None,
    button_color = None,
    disabled = False,
    font = None,
    tooltip = None,
    bind_return_key = False,
    focus = False,
    pad = None,
    p = None,
    key = None,
    k = None,
    visible = True,
    metadata = None,
    expand_x = False,
    expand_y = False)
```

Parameter Descriptions:

Type

Name

Meaning

str

button_text

text in the button (Default value = 'Help')

(int, int)

size

(w,h) w=characters-wide, h=rows-high

(int, int) or (None, None) or int

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

bool

auto_size_button

True if button size is determined by button text

(str, str) or str

button_color

button color (foreground, background)

bool

disabled

set disable state for element (Default = False)

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

str

tooltip

text, that will appear when mouse hovers over the element

bool

bind_return_key

(Default = False) If True, then the return key will cause a the Listbox to generate an event

focus

if focus should be set to this

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

str or int or tuple or object

key

key for uniquely identify this element (for window.find_element)

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

bool

visible

set initial visibility state of the Button

Any

metadata

Anything you want to store along with this button

bool

expand_x

If True Element will expand in the Horizontal directions

bool

expand_y

If True Element will expand in the Vertical directions

(Button)

**RETURN**

returns a button

```
No(button_text = "No",
    size = (None, None),
    s = (None, None),
    auto_size_button = None,
    button_color = None,
    disabled = False,
    tooltip = None,
    font = None,
    bind_return_key = False,
    focus = False,
    pad = None,
    p = None,
    key = None,
    k = None,
    visible = True,
    metadata = None,
    expand_x = False,
    expand_y = False)
```

Parameter Descriptions:

Type

Name

Meaning

str

button_text

text in the button (Default value = 'No')

(int, int)

size

(w,h) w=characters-wide, h=rows-high

(int, int) or (None, None) or int

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

bool

auto_size_button

True if button size is determined by button text

(str, str) or str

button_color

button color (foreground, background)

bool

disabled

set disable state for element (Default = False)

str

tooltip

text, that will appear when mouse hovers over the element

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

bind_return_key

(Default = False) If True, then the return key will cause a the Listbox to generate an event

focus

if focus should be set to this

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

str or int or tuple or object

key

key for uniquely identify this element (for window.find_element)

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

bool

visible

set initial visibility state of the Button

Any

metadata

Anything you want to store along with this button

bool

expand_x

If True Element will expand in the Horizontal directions

bool

expand_y

If True Element will expand in the Vertical directions

(Button)

**RETURN**

returns a button

```
OK(button_text = "OK",
    size = (None, None),
    s = (None, None),
    auto_size_button = None,
    button_color = None,
    disabled = False,
    bind_return_key = True,
    tooltip = None,
    font = None,
    focus = False,
    pad = None,
    p = None,
    key = None,
    k = None,
    visible = True,
    metadata = None,
    expand_x = False,
    expand_y = False)
```

Parameter Descriptions:

Type

Name

Meaning

str

button_text

text in the button (Default value = 'OK')

(int, int)

size

(w,h) w=characters-wide, h=rows-high

(int, int) or (None, None) or int

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

bool

auto_size_button

True if button size is determined by button text

(str, str) or str

button_color

button color (foreground, background)

bool

disabled

set disable state for element (Default = False)

bool

bind_return_key

(Default = True) If True, then the return key will cause a the Listbox to generate an event

str

tooltip

text, that will appear when mouse hovers over the element

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

idk_yetReally

focus

if focus should be set to this

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

str or int or tuple or object

key

key for uniquely identify this element (for window.find_element)

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

bool

visible

set initial visibility state of the Button

Any

metadata

Anything you want to store along with this button

bool

expand_x

If True Element will expand in the Horizontal directions

bool

expand_y

If True Element will expand in the Vertical directions

(Button)

**RETURN**

returns a button

```
Ok(button_text = "Ok",
    size = (None, None),
    s = (None, None),
    auto_size_button = None,
    button_color = None,
    disabled = False,
    bind_return_key = True,
    tooltip = None,
    font = None,
    focus = False,
    pad = None,
    p = None,
    key = None,
    k = None,
    visible = True,
    metadata = None,
    expand_x = False,
    expand_y = False)
```

Parameter Descriptions:

Type

Name

Meaning

str

button_text

text in the button (Default value = 'Ok')

(int, int)

size

(w,h) w=characters-wide, h=rows-high

(int, int) or (None, None) or int

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

bool

auto_size_button

True if button size is determined by button text

(str, str) or str

button_color

button color (foreground, background)

bool

disabled

set disable state for element (Default = False)

bool

bind_return_key

(Default = True) If True, then the return key will cause a the Listbox to generate an event

str

tooltip

text, that will appear when mouse hovers over the element

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

idk_yetReally

focus

if focus should be set to this

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

str or int or tuple or object

key

key for uniquely identify this element (for window.find_element)

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

bool

visible

set initial visibility state of the Button

Any

metadata

Anything you want to store along with this button

bool

expand_x

If True Element will expand in the Horizontal directions

bool

expand_y

If True Element will expand in the Vertical directions

(Button)

**RETURN**

returns a button

```
Open(button_text = "Open",
    size = (None, None),
    s = (None, None),
    auto_size_button = None,
    button_color = None,
    disabled = False,
    bind_return_key = True,
    tooltip = None,
    font = None,
    focus = False,
    pad = None,
    p = None,
    key = None,
    k = None,
    visible = True,
    metadata = None,
    expand_x = False,
    expand_y = False)
```

Parameter Descriptions:

Type

Name

Meaning

str

button_text

text in the button (Default value = 'Open')

(int, int)

size

(w,h) w=characters-wide, h=rows-high

(int, int) or (None, None) or int

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

bool

auto_size_button

True if button size is determined by button text

(str, str) or str

button_color

button color (foreground, background)

bool

disabled

set disable state for element (Default = False)

bool

bind_return_key

(Default = True) If True, then the return key will cause a the Listbox to generate an event

str

tooltip

text, that will appear when mouse hovers over the element

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

idk_yetReally

focus

if focus should be set to this

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

str or int or tuple or object

key

key for uniquely identify this element (for window.find_element)

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

bool

visible

set initial visibility state of the Button

Any

metadata

Anything you want to store along with this button

bool

expand_x

If True Element will expand in the Horizontal directions

bool

expand_y

If True Element will expand in the Vertical directions

(Button)

**RETURN**

returns a button

```
Quit(button_text = "Quit",
    size = (None, None),
    s = (None, None),
    auto_size_button = None,
    button_color = None,
    disabled = False,
    tooltip = None,
    font = None,
    bind_return_key = False,
    focus = False,
    pad = None,
    p = None,
    key = None,
    k = None,
    visible = True,
    metadata = None,
    expand_x = False,
    expand_y = False)
```

Parameter Descriptions:

Type

Name

Meaning

str

button_text

text in the button (Default value = 'Quit')

(int, int)

size

(w,h) w=characters-wide, h=rows-high

(int, int) or (None, None) or int

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

bool

auto_size_button

True if button size is determined by button text

(str, str) or str

button_color

button color (foreground, background)

bool

disabled

set disable state for element (Default = False)

str

tooltip

text, that will appear when mouse hovers over the element

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

bind_return_key

(Default = False) If True, then the return key will cause a the Listbox to generate an event

bool

focus

if focus should be set to this

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

str or int or tuple or object

key

key for uniquely identify this element (for window.find_element)

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

bool

visible

set initial visibility state of the Button

Any

metadata

Anything you want to store along with this button

bool

expand_x

If True Element will expand in the Horizontal directions

bool

expand_y

If True Element will expand in the Vertical directions

(Button)

**RETURN**

returns a button

```
RealtimeButton(button_text,
    image_filename = None,
    image_data = None,
    image_size = (None, None),
    image_subsample = None,
    border_width = None,
    tooltip = None,
    size = (None, None),
    s = (None, None),
    auto_size_button = None,
    button_color = None,
    font = None,
    disabled = False,
    bind_return_key = False,
    focus = False,
    pad = None,
    p = None,
    key = None,
    k = None,
    visible = True,
    metadata = None,
    expand_x = False,
    expand_y = False)
```

Parameter Descriptions:

Type

Name

Meaning

str

button_text

text in the button

image filename if there is a button image

image_filename

image filename if there is a button image

in-RAM image to be displayed on button

image_data

in-RAM image to be displayed on button

(Default = (None))

image_size

image size (O.K.)

amount to reduce the size of the image

image_subsample

amount to reduce the size of the image

int

border_width

width of border around element

str

tooltip

text, that will appear when mouse hovers over the element

(int, int)

size

(w,h) w=characters-wide, h=rows-high

(int, int) or (None, None) or int

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

bool

auto_size_button

True if button size is determined by button text

(str, str) or str

button_color

button color (foreground, background)

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

disabled

set disable state for element (Default = False)

bool

bind_return_key

(Default = False) If True, then the return key will cause a the Listbox to generate an event

bool

focus

if focus should be set to this

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

str or int or tuple or object

key

key for uniquely identify this element (for window.find_element)

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

bool

visible

set initial visibility state of the Button

Any

metadata

Anything you want to store along with this button

bool

expand_x

If True Element will expand in the Horizontal directions

bool

expand_y

If True Element will expand in the Vertical directions

(Button)

**RETURN**

Button created

```
Save(button_text = "Save",
    size = (None, None),
    s = (None, None),
    auto_size_button = None,
    button_color = None,
    bind_return_key = True,
    disabled = False,
    tooltip = None,
    font = None,
    focus = False,
    pad = None,
    p = None,
    key = None,
    k = None,
    visible = True,
    metadata = None,
    expand_x = False,
    expand_y = False)
```

Parameter Descriptions:

Type

Name

Meaning

str

button_text

text in the button (Default value = 'Save')

(int, int)

size

(w,h) w=characters-wide, h=rows-high

(int, int) or (None, None) or int

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

bool

auto_size_button

True if button size is determined by button text

(str, str) or str

button_color

button color (foreground, background)

bool

bind_return_key

(Default = True) If True, then the return key will cause a the Listbox to generate an event

bool

disabled

set disable state for element (Default = False)

str

tooltip

text, that will appear when mouse hovers over the element

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

idk_yetReally

focus

if focus should be set to this

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

str or int or tuple or object

key

key for uniquely identify this element (for window.find_element)

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

bool

visible

set initial visibility state of the Button

Any

metadata

Anything you want to store along with this button

bool

expand_x

If True Element will expand in the Horizontal directions

bool

expand_y

If True Element will expand in the Vertical directions

(Button)

**RETURN**

returns a button

```
SaveAs(button_text = "Save As...",
    target = (555666777, -1),
    file_types = (('ALL Files', '*.* *'),),
    initial_folder = None,
    default_extension = "",
    disabled = False,
    tooltip = None,
    size = (None, None),
    s = (None, None),
    auto_size_button = None,
    button_color = None,
    change_submits = False,
    enable_events = False,
    font = None,
    pad = None,
    p = None,
    key = None,
    k = None,
    visible = True,
    metadata = None,
    expand_x = False,
    expand_y = False)
```

Parameter Descriptions:

Type

Name

Meaning

str

button_text

text in the button (Default value = 'Save As...')

str or (int, int)

target

key or (row,col) target for the button (Default value = (ThisRow, -1))

Tuple[(str, str), ...]

file_types

Default value = (("ALL Files", "_._ *"),).

str

default_extension

If no extension entered by user, add this to filename (only used in saveas dialogs)

str

initial_folder

starting path for folders and files

bool

disabled

set disable state for element (Default = False)

str

tooltip

text, that will appear when mouse hovers over the element

(int, int)

size

(w,h) w=characters-wide, h=rows-high

(int, int) or (None, None) or int

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

bool

auto_size_button

True if button size is determined by button text

(str, str) or str

button_color

button color (foreground, background)

bool

change_submits

If True, pressing Enter key submits window (Default = False)

bool

enable_events

Turns on the element specific events.(Default = False)

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int :param key: key for uniquely identify this element (for window.find_element)

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

bool

visible

set initial visibility state of the Button

Any

metadata

Anything you want to store along with this button

bool

expand_x

If True Element will expand in the Horizontal directions

bool

expand_y

If True Element will expand in the Vertical directions

(Button)

**RETURN**

returns a button

```
Submit(button_text = "Submit",
    size = (None, None),
    s = (None, None),
    auto_size_button = None,
    button_color = None,
    disabled = False,
    bind_return_key = True,
    tooltip = None,
    font = None,
    focus = False,
    pad = None,
    p = None,
    key = None,
    k = None,
    visible = True,
    metadata = None,
    expand_x = False,
    expand_y = False)
```

Parameter Descriptions:

Type

Name

Meaning

str

button_text

text in the button (Default value = 'Submit')

(int, int)

size

(w,h) w=characters-wide, h=rows-high

(int, int) or (None, None) or int

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

bool

auto_size_button

True if button size is determined by button text

(str, str) or str

button_color

button color (foreground, background)

bool

disabled

set disable state for element (Default = False)

bool

bind_return_key

(Default = True) If True, then the return key will cause a the Listbox to generate an event

str

tooltip

text, that will appear when mouse hovers over the element

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

idk_yetReally

focus

if focus should be set to this

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

str or int or tuple or object

key

key for uniquely identify this element (for window.find_element)

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

bool

visible

set initial visibility state of the Button

Any

metadata

Anything you want to store along with this button

bool

expand_x

If True Element will expand in the Horizontal directions

bool

expand_y

If True Element will expand in the Vertical directions

(Button)

**RETURN**

returns a button

```
Yes(button_text = "Yes",
    size = (None, None),
    s = (None, None),
    auto_size_button = None,
    button_color = None,
    disabled = False,
    tooltip = None,
    font = None,
    bind_return_key = True,
    focus = False,
    pad = None,
    p = None,
    key = None,
    k = None,
    visible = True,
    metadata = None,
    expand_x = False,
    expand_y = False)
```

Parameter Descriptions:

Type

Name

Meaning

str

button_text

text in the button (Default value = 'Yes')

(int, int)

size

(w,h) w=characters-wide, h=rows-high

(int, int) or (None, None) or int

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

bool

auto_size_button

True if button size is determined by button text

(str, str) or str

button_color

button color (foreground, background)

bool

disabled

set disable state for element (Default = False)

str

tooltip

text, that will appear when mouse hovers over the element

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

bind_return_key

(Default = True) If True, then the return key will cause a the Listbox to generate an event

focus

if focus should be set to this

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

str or int or tuple or object

key

key for uniquely identify this element (for window.find_element)

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

bool

visible

set initial visibility state of the Button

Any

metadata

Anything you want to store along with this button

bool

expand_x

If True Element will expand in the Horizontal directions

bool

expand_y

If True Element will expand in the Vertical directions

(Button)

**RETURN**

returns a button

[Back](./_Elements)
