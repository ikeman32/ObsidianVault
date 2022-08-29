# Window
```
Represents a single Window
```

```
Window(title,
    layout = None,
    default_element_size = None,
    default_button_element_size = (None, None),
    auto_size_text = None,
    auto_size_buttons = None,
    location = (None, None),
    relative_location = (None, None),
    size = (None, None),
    element_padding = None,
    margins = (None, None),
    button_color = None,
    font = None,
    progress_bar_color = (None, None),
    background_color = None,
    border_depth = None,
    auto_close = False,
    auto_close_duration = 3,
    icon = None,
    force_toplevel = False,
    alpha_channel = None,
    return_keyboard_events = False,
    use_default_focus = True,
    text_justification = None,
    no_titlebar = False,
    grab_anywhere = False,
    grab_anywhere_using_control = True,
    keep_on_top = None,
    resizable = False,
    disable_close = False,
    disable_minimize = False,
    right_click_menu = None,
    transparent_color = None,
    debugger_enabled = True,
    right_click_menu_background_color = None,
    right_click_menu_text_color = None,
    right_click_menu_disabled_text_color = None,
    right_click_menu_selected_colors = (None, None),
    right_click_menu_font = None,
    right_click_menu_tearoff = False,
    finalize = False,
    element_justification = "left",
    ttk_theme = None,
    use_ttk_buttons = None,
    modal = False,
    enable_close_attempted_event = False,
    enable_window_config_events = False,
    titlebar_background_color = None,
    titlebar_text_color = None,
    titlebar_font = None,
    titlebar_icon = None,
    use_custom_titlebar = None,
    scaling = None,
    sbar_trough_color = None,
    sbar_background_color = None,
    sbar_arrow_color = None,
    sbar_width = None,
    sbar_arrow_width = None,
    sbar_frame_color = None,
    sbar_relief = None,
    metadata = None)
```

Parameter Descriptions:

Type

Name

Meaning

str

title

The title that will be displayed in the Titlebar and on the Taskbar

List[List[Element]] or Tuple[Tuple[Element]]

layout

The layout for the window. Can also be specified in the Layout method

(int, int) - (width, height)

default_element_size

size in characters (wide) and rows (high) for all elements in this window

(int, int)

default_button_element_size

(width, height) size in characters (wide) and rows (high) for all Button elements in this window

bool

auto_size_text

True if Elements in Window should be sized to exactly fir the length of text

bool

auto_size_buttons

True if Buttons in this Window should be sized to exactly fit the text on this.

(int, int)

relative_location

(x,y) location relative to the default location of the window, in pixels. Normally the window centers. This location is relative to the location the window would be created. Note they can be negative.

(int, int or None, None) or None

location

(x,y) location, in pixels, to locate the upper left corner of the window on the screen. Default is to center on screen. None will not set any location meaning the OS will decide

(int, int)

size

(width, height) size in pixels for this window. Normally the window is autosized to fit contents, not set to an absolute size by the user. Try not to set this value. You risk, the contents being cut off, etc. Let the layout determine the window size instead

(int, int or (int, int),(int,int)) or int

element_padding

Default amount of padding to put around elements in window (left/right, top/bottom) or ((left, right), (top, bottom)), or an int. If an int, then it's converted into a tuple (int, int)

(int, int)

margins

(left/right, top/bottom) Amount of pixels to leave inside the window's frame around the edges before your elements are shown.

(str, str) or str

button_color

Default button colors for all buttons in the window

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

(str, str)

progress_bar_color

(bar color, background color) Sets the default colors for all progress bars in the window

str

background_color

color of background

int

border_depth

Default border depth (width) for all elements in the window

bool

auto_close

If True, the window will automatically close itself

int

auto_close_duration

Number of seconds to wait before closing the window

(str or bytes)

icon

Can be either a filename or Base64 value. For Windows if filename, it MUST be ICO format. For Linux, must NOT be ICO. Most portable is to use a Base64 of a PNG file. This works universally across all OS's

bool

force_toplevel

If True will cause this window to skip the normal use of a hidden master window

float

alpha_channel

Sets the opacity of the window. 0 = invisible 1 = completely visible. Values bewteen 0 & 1 will produce semi-transparent windows in SOME environments (The Raspberry Pi always has this value at 1 and cannot change.

bool

return_keyboard_events

if True key presses on the keyboard will be returned as Events from Read calls

bool

use_default_focus

If True will use the default focus algorithm to set the focus to the "Correct" element

'left' or 'right' or 'center'

text_justification

Default text justification for all Text Elements in window

bool

no_titlebar

If true, no titlebar nor frame will be shown on window. This means you cannot minimize the window and it will not show up on the taskbar

bool

grab_anywhere

If True can use mouse to click and drag to move the window. Almost every location of the window will work except input fields on some systems

bool

grab_anywhere_using_control

If True can use CONTROL key + left mouse mouse to click and drag to move the window. DEFAULT is TRUE. Unlike normal grab anywhere, it works on all elements.

bool

keep_on_top

If True, window will be created on top of all other windows on screen. It can be bumped down if another window created with this parm

bool

resizable

If True, allows the user to resize the window. Note the not all Elements will change size or location when resizing.

bool

disable_close

If True, the X button in the top right corner of the window will no work. Use with caution and always give a way out toyour users

bool

disable_minimize

if True the user won't be able to minimize window. Good for taking over entire screen and staying that way.

List[List[ List[str] or str ]]

right_click_menu

A list of lists of Menu items to show when this element is right clicked. See user docs for exact format.

str

transparent_color

Any portion of the window that has this color will be completely transparent. You can even click through these spots to the window under this window.

bool

debugger_enabled

If True then the internal debugger will be enabled

str

right_click_menu_background_color

Background color for right click menus

str

right_click_menu_text_color

Text color for right click menus

str

right_click_menu_disabled_text_color

Text color for disabled right click menu items

(str, str) or str or Tuple

right_click_menu_selected_colors

Text AND background colors for a selected item. Can be a Tuple OR a color string. simplified-button-color-string "foreground on background". Can be a single color if want to set only the background. Normally a tuple, but can be a simplified-dual-color-string "foreground on background". Can be a single color if want to set only the background.

(str or (str, int[, str]) or None)

right_click_menu_font

Font for right click menus

bool

right_click_menu_tearoff

If True then all right click menus can be torn off

bool

finalize

If True then the Finalize method will be called. Use this rather than chaining .Finalize for cleaner code

str

element_justification

All elements in the Window itself will have this justification 'left', 'right', 'center' are valid values

str

ttk_theme

Set the tkinter ttk "theme" of the window. Default = DEFAULT_TTK_THEME. Sets all ttk widgets to this theme as their default

bool

use_ttk_buttons

Affects all buttons in window. True = use ttk buttons. False = do not use ttk buttons. None = use ttk buttons only if on a Mac

bool

modal

If True then this window will be the only window a user can interact with until it is closed

bool

enable_close_attempted_event

If True then the window will not close when "X" clicked. Instead an event WINDOW_CLOSE_ATTEMPTED_EVENT if returned from window.read

bool

enable_window_config_events

If True then window configuration events (resizing or moving the window) will return WINDOW_CONFIG_EVENT from window.read. Note you will get several when Window is created.

(str or None)

titlebar_background_color

If custom titlebar indicated by use_custom_titlebar, then use this as background color

(str or None)

titlebar_text_color

If custom titlebar indicated by use_custom_titlebar, then use this as text color

(str or (str, int[, str]) or None)

titlebar_font

If custom titlebar indicated by use_custom_titlebar, then use this as title font

(bytes or str)

titlebar_icon

If custom titlebar indicated by use_custom_titlebar, then use this as the icon (file or base64 bytes)

bool

use_custom_titlebar

If True, then a custom titlebar will be used instead of the normal titlebar

float

scaling

Apply scaling to the elements in the window. Can be set on a global basis using set_options

str

sbar_trough_color

Scrollbar color of the trough

str

sbar_background_color

Scrollbar color of the background of the arrow buttons at the ends AND the color of the "thumb" (the thing you grab and slide). Switches to arrow color when mouse is over

str

sbar_arrow_color

Scrollbar color of the arrow at the ends of the scrollbar (it looks like a button). Switches to background color when mouse is over

int

sbar_width

Scrollbar width in pixels

int

sbar_arrow_width

Scrollbar width of the arrow on the scrollbar. It will potentially impact the overall width of the scrollbar

str

sbar_frame_color

Scrollbar Color of frame around scrollbar (available only on some ttk themes)

str

sbar_relief

Scrollbar relief that will be used for the "thumb" of the scrollbar (the thing you grab that slides). Should be a constant that is defined at starting with "RELIEF_" - RELIEF_RAISED, RELIEF_SUNKEN, RELIEF_FLAT, RELIEF_RIDGE, RELIEF_GROOVE, RELIEF_SOLID

Any

metadata

User metadata that can be set to ANYTHING

### add_row

Adds a single row of elements to a window's self.Rows variables. Generally speaking this is NOT how users should be building Window layouts. Users, create a single layout (a list of lists) and pass as a parameter to Window object, or call Window.Layout(layout)

```
add_row(args=*<1 or N object>)
```

Parameter Descriptions:

Type

Name

Meaning

*args

List[Elements]

### add_rows

Loops through a list of lists of elements and adds each row, list, to the layout. This is NOT the best way to go about creating a window. Sending the entire layout at one time and passing it as a parameter to the Window call is better.

```
add_rows(rows)
```

Parameter Descriptions:

Type

Name

Meaning

List[List[Elements]]

rows

A list of a list of elements

### alpha_channel

#### property: alpha_channel

A property that changes the current alpha channel value (internal value)

Type

Name

Meaning

(float)

**return**

the current alpha channel setting according to self, not read directly from tkinter

### bind

Used to add tkinter events to a Window. The tkinter specific data is in the Window's member variable user_bind_event

```
bind(bind_string,
    key,
    propagate = True)
```

Parameter Descriptions:

Type

Name

Meaning

str

bind_string

The string tkinter expected in its bind function

str or int or tuple or object

key

The event that will be generated when the tkinter event occurs

bool

propagate

If True then tkinter will be told to propagate the event

### bring_to_front

Brings this window to the top of all other windows (perhaps may not be brought before a window made to "stay on top")

```python
bring_to_front()
```

### close

Closes window. Users can safely call even if window has been destroyed. Should always call when done with a window so that resources are properly freed up within your thread.

```python
close()
```

### current_location

Get the current location of the window's top left corner. Sometimes, depending on the environment, the value returned does not include the titlebar,etc A new option, more_accurate, can be used to get the theoretical upper leftmost corner of the window. The titlebar and menubar are crated by the OS. It gets really confusing when running in a webpage (repl, trinket) Thus, the values can appear top be "off" due to the sometimes unpredictable way the location is calculated. If without_titlebar is set then the location of the root x,y is used which should not include the titlebar but may be OS dependent.

```
current_location(more_accurate = False, without_titlebar = False)
```

Parameter Descriptions:

Type

Name

Meaning

bool

more_accurate

If True, will use the window's geometry to get the topmost location with titlebar, menubar taken into account

bool

without_titlebar

If True, return location of top left of main window area without the titlebar (may be OS dependent?)

Tuple[(int or None), (int or None)]

**RETURN**

The x and y location in tuple form (x,y)

### ding

Make a "bell" sound. A capability provided by tkinter. Your window needs to be finalized prior to calling. Ring a display's bell is the tkinter description of the call.

```
ding(display_number = 0)
```

Parameter Descriptions:

Type

Name

Meaning

int

display_number

Passed to tkinter's bell method as parameter "displayof".

### disable

Disables window from taking any input from the user

```python
disable()
```

### disable_debugger

Disable the internal debugger. By default the debugger is ENABLED

```python
disable_debugger()
```

### disappear

Causes a window to "disappear" from the screen, but remain on the taskbar. It does this by turning the alpha channel to 0. NOTE that on some platforms alpha is not supported. The window will remain showing on these platforms. The Raspberry Pi for example does not have an alpha setting

```python
disappear()
```

### elem

### element

### element_list

Returns a list of all elements in the window

`element_list()`

Type

Name

Meaning

List[Element]

**return**

List of all elements in the window and container elements in the window

### enable

Re-enables window to take user input after having it be Disabled previously

```python
enable()
```

### enable_debugger

Enables the internal debugger. By default, the debugger IS enabled

```python
enable_debugger()
```

### extend_layout

Adds new rows to an existing container element inside of this window If the container is a scrollable Column, you need to also call the contents_changed() method

```
extend_layout(container, rows)
```

Parameter Descriptions:

Type

Name

Meaning

Frame or Column or Tab

container

The container Element the layout will be placed inside of

(List[List[Element]])

rows

The layout to be added

(Window)

**RETURN**

(Window) self so could be chained

### fill

Fill in elements that are input fields with data based on a 'values dictionary'

```
fill(values_dict)
```

Parameter Descriptions:

Type

Name

Meaning

(Dict[Any, Any]) - {Element_key : value}

values_dict

pairs

(Window)

**RETURN**

returns self so can be chained with other methods

### finalize

Use this method to cause your layout to built into a real tkinter window. In reality this method is like Read(timeout=0). It doesn't block and uses your layout to create tkinter widgets to represent the elements. Lots of action!

`finalize()`

Type

Name

Meaning

(Window)

**return**

Returns 'self' so that method "Chaining" can happen (read up about it as it's very cool!)

### find

### find_element

Find element object associated with the provided key. THIS METHOD IS NO LONGER NEEDED to be called by the user

You can perform the same operation by writing this statement: element = window[key]

You can drop the entire "find_element" function name and use [ ] instead.

However, if you wish to perform a lookup without error checking, and don't have error popups turned off globally, you'll need to make this call so that you can disable error checks on this call.

find_element is yypically used in combination with a call to element's Update method (or any other element method!): window[key].update(new_value)

Versus the "old way" window.FindElement(key).Update(new_value)

This call can be abbreviated to any of these: find_element = FindElement == Element == Find With find_element being the PEP8 compliant call that should be used.

Rememeber that this call will return None if no match is found which may cause your code to crash if not checked for.

```
find_element(key, silent_on_error = False)
```

Parameter Descriptions:

Type

Name

Meaning

str or int or tuple or object

key

Used with window.find_element and with return values to uniquely identify this element

bool

silent_on_error

If True do not display popup nor print warning of key errors

Element or Error Element or None

**RETURN**

Return value can be: the Element that matches the supplied key if found; an Error Element if silent_on_error is False; None if silent_on_error True;

### find_element_with_focus

Returns the Element that currently has focus as reported by tkinter. If no element is found None is returned!

`find_element_with_focus()`

Type

Name

Meaning

Element

None

**return**

### force_focus

Forces this window to take focus

```python
force_focus()
```

### get_screen_dimensions

Get the screen dimensions. NOTE - you must have a window already open for this to work (blame tkinter not me)

`get_screen_dimensions()`

Type

Name

Meaning

Tuple[None, None]

Tuple[width, height]

**return**

### get_screen_size

This is a "Class Method" meaning you call it by writing: width, height = Window.get_screen_size() Returns the size of the "screen" as determined by tkinter. This can vary depending on your operating system and the number of monitors installed on your system. For Windows, the primary monitor's size is returns. On some multi-monitored Linux systems, the monitors are combined and the total size is reported as if one screen.

```
get_screen_size()
```

Parameter Descriptions:

Type

Name

Meaning

(int, int)

**RETURN**

Size of the screen in pixels as determined by tkinter

### grab_any_where_off

Turns off Grab Anywhere functionality AFTER a window has been created. Don't try on a window that's not yet been Finalized or Read.

```python
grab_any_where_off()
```

### grab_any_where_on

Turns on Grab Anywhere functionality AFTER a window has been created. Don't try on a window that's not yet been Finalized or Read.

```python
grab_any_where_on()
```

### hide

Hides the window from the screen and the task bar

```python
hide()
```

### keep_on_top_clear

Clears keep_on_top after a window has been created. Effect is the same as if the window was created with this set.

```python
keep_on_top_clear()
```

### keep_on_top_set

Sets keep_on_top after a window has been created. Effect is the same as if the window was created with this set. The Window is also brought to the front

```python
keep_on_top_set()
```

### key_dict

#### property: key_dict

Returns a dictionary with all keys and their corresponding elements { key : Element }

Type

Name

Meaning

Dict[Any, Element]

**return**

Dictionary of keys and elements

### layout

Second of two preferred ways of telling a Window what its layout is. The other way is to pass the layout as a parameter to Window object. The parameter method is the currently preferred method. This call to Layout has been removed from examples contained in documents and in the Demo Programs. Trying to remove this call from history and replace with sending as a parameter to Window.

```
layout(rows)
```

Parameter Descriptions:

Type

Name

Meaning

List[List[Elements]]

rows

Your entire layout

(Window)

**RETURN**

self so that you can chain method calls

### load_from_disk

Restore values from a previous call to SaveToDisk which saves the returned values dictionary in Pickle format

```
load_from_disk(filename)
```

Parameter Descriptions:

Type

Name

Meaning

str

filename

Pickle Filename to load

### make_modal

Makes a window into a "Modal Window" This means user will not be able to interact with other windows until this one is closed

```
    NOTE - Sorry Mac users - you can't have modal windows.... lobby your tkinter Mac devs
```

```python
make_modal()
```

### maximize

Maximize the window. This is done differently on a windows system versus a linux or mac one. For non-Windows the root attribute '-fullscreen' is set to True. For Windows the "root" state is changed to "zoomed" The reason for the difference is the title bar is removed in some cases when using fullscreen option

```python
maximize()
```

### key

#### property: key

Returns key for the element. This is a READONLY property. Keys can be any hashable object (basically anything except a list... tuples are ok, but not lists)

Type

Name

Meaning

(Any)

**return**

The window's Key

### metadata

#### property: metadata

Metadata is available for all windows. You can set to any value.

Type

Name

Meaning

(Any)

**return**

the current metadata value

### minimize

Minimize this window to the task bar

```python
minimize()
```

### mouse_location

Return the (x,y) location of the mouse relative to the entire screen. It's the same location that you would use to create a window, popup, etc.

`mouse_location()`

Type

Name

Meaning

(int, int)

**return**

The location of the mouse pointer

### move

Move the upper left corner of this window to the x,y coordinates provided

```
move(x, y)
```

Parameter Descriptions:

Type

Name

Meaning

int

x

x coordinate in pixels

int

y

y coordinate in pixels

### move_to_center

Recenter your window after it's been moved or the size changed.

```
    This is a conveinence method. There are no tkinter calls involved, only pure PySimpleGUI API calls.
```

```python
move_to_center()
```

### normal

Restore a window to a non-maximized state. Does different things depending on platform. See Maximize for more.

```python
normal()
```

### perform_long_operation

Call your function that will take a long time to execute. When it's complete, send an event specified by the end_key.

Starts a thread on your behalf.

This is a way for you to "ease into" threading without learning the details of threading. Your function will run, and when it returns 2 things will happen: 1. The value you provide for end_key will be returned to you when you call window.read() 2. If your function returns a value, then the value returned will also be included in your windows.read call in the values dictionary

IMPORTANT - This method uses THREADS... this means you CANNOT make any PySimpleGUI calls from the function you provide with the exception of one function, Window.write_event_value.

```
perform_long_operation(func, end_key)
```

Parameter Descriptions:

Type

Name

Meaning

Any

func

A lambda or a function name with no parms

Any

end_key

The key that will be generated when the function returns

threading.Thread

**RETURN**

The id of the thread

### read

THE biggest deal method in the Window class! This is how you get all of your data from your Window. Pass in a timeout (in milliseconds) to wait for a maximum of timeout milliseconds. Will return timeout_key if no other GUI events happen first.

```
read(timeout = None,
    timeout_key = "__TIMEOUT__",
    close = False)
```

Parameter Descriptions:

Type

Name

Meaning

int

timeout

Milliseconds to wait until the Read will return IF no other GUI events happen first

Any

timeout_key

The value that will be returned from the call if the timer expired

bool

close

if True the window will be closed prior to returning

Tuple[(Any), Dict[Any, Any], List[Any], None]

**RETURN**

(event, values)

### reappear

Causes a window previously made to "Disappear" (using that method). Does this by restoring the alpha channel

```python
reappear()
```

### refresh

Refreshes the window by calling tkroot.update(). Can sometimes get away with a refresh instead of a Read. Use this call when you want something to appear in your Window immediately (as soon as this function is called). If you change an element in a window, your change will not be visible until the next call to Window.read or a call to Window.refresh()

`refresh()`

Type

Name

Meaning

(Window)

**return**

`self` so that method calls can be easily "chained"

### save_to_disk

Saves the values contained in each of the input areas of the form. Basically saves what would be returned from a call to Read. It takes these results and saves them to disk using pickle. Note that every element in your layout that is to be saved must have a key assigned to it.

```
save_to_disk(filename)
```

Parameter Descriptions:

Type

Name

Meaning

str

filename

Filename to save the values to in pickled form

### save_window_screenshot_to_disk

Saves an image of the PySimpleGUI window provided into the filename provided

```
save_window_screenshot_to_disk(filename = None)
```

Parameter Descriptions:

Type

Name

Meaning

(PIL.ImageGrab or None)

**RETURN**

A PIL ImageGrab object that can be saved or manipulated

### send_to_back

Pushes this window to the bottom of the stack of windows. It is the opposite of BringToFront

```python
send_to_back()
```

### set_alpha

Sets the Alpha Channel for a window. Values are between 0 and 1 where 0 is completely transparent

```
set_alpha(alpha)
```

Parameter Descriptions:

Type

Name

Meaning

float

alpha

0 to 1. 0 is completely transparent. 1 is completely visible and solid (can't see through)

### set_cursor

Sets the cursor for the window. If you do not want any mouse pointer, then use the string "none"

```
set_cursor(cursor)
```

Parameter Descriptions:

Type

Name

Meaning

str

cursor

The tkinter cursor name

### set_icon

Changes the icon that is shown on the title bar and on the task bar. NOTE - The file type is IMPORTANT and depends on the OS! Can pass in: * filename which must be a .ICO icon file for windows, PNG file for Linux * bytes object * BASE64 encoded file held in a variable

```
set_icon(icon = None, pngbase64 = None)
```

Parameter Descriptions:

Type

Name

Meaning

str

icon

Filename or bytes object

bytes

pngbase64

Base64 encoded image

### set_min_size

Changes the minimum size of the window. Note Window must be read or finalized first.

```
set_min_size(size)
```

Parameter Descriptions:

Type

Name

Meaning

(int, int)

size

(width, height) tuple (int, int) of the desired window size in pixels

### set_size

Changes the size of the window, if possible. You can also use the Window.size prooerty to set/get the size.

```
set_size(size)
```

Parameter Descriptions:

Type

Name

Meaning

(int, int)

size

(width, height) of the desired window size

### set_title

Change the title of the window

```
set_title(title)
```

Parameter Descriptions:

Type

Name

Meaning

str

title

The string to set the title to

### set_transparent_color

Set the color that will be transparent in your window. Areas with this color will be SEE THROUGH.

```
set_transparent_color(color)
```

Parameter Descriptions:

Type

Name

Meaning

str

color

Color string that defines the transparent color

### size

#### property: size

Return the current size of the window in pixels

Type

Name

Meaning

Tuple[(int), (int)] or Tuple[None, None]

**return**

(width, height) of the window

### start_thread

Call your function that will take a long time to execute. When it's complete, send an event specified by the end_key.

Starts a thread on your behalf.

This is a way for you to "ease into" threading without learning the details of threading. Your function will run, and when it returns 2 things will happen: 1. The value you provide for end_key will be returned to you when you call window.read() 2. If your function returns a value, then the value returned will also be included in your windows.read call in the values dictionary

IMPORTANT - This method uses THREADS... this means you CANNOT make any PySimpleGUI calls from the function you provide with the exception of one function, Window.write_event_value.

```
start_thread(func, end_key)
```

Parameter Descriptions:

Type

Name

Meaning

Any

func

A lambda or a function name with no parms

Any

end_key

The key that will be generated when the function returns

threading.Thread

**RETURN**

The id of the thread

### un_hide

Used to bring back a window that was previously hidden using the Hide method

```python
un_hide()
```

### visibility_changed

When making an element in a column or someplace that has a scrollbar, then you'll want to call this function prior to the column's contents_changed() method.

```python
visibility_changed()
```

### was_closed

Returns True if the window was closed

`was_closed()`

Type

Name

Meaning

bool

**return**

True if the window is closed

### widget_to_element

Returns the element that matches a supplied tkinter widget. If no matching element is found, then None is returned.

```
widget_to_element(widget)
```

Parameter Descriptions:

Type

Name

Meaning

Element or None

**RETURN**

Element that uses the specified widget

### write_event_value

Adds a key & value tuple to the queue that is used by threads to communicate with the window

```
write_event_value(key, value)
```

Parameter Descriptions:

Type

Name

Meaning

Any

key

The key that will be returned as the event when reading the window

Any

value

The value that will be in the values dictionary

---

### These are non-PEP8 Compliant Methods - do NOT use

**_Do not use these_**... they are here for your reference should you see them in old code.

The following methods are here for backwards compatibility reference. You will find there are PEP8 versions for each of these methods. The PEP8 versions will be all lower case and have underscores.

### AddRow

Adds a single row of elements to a window's self.Rows variables. Generally speaking this is NOT how users should be building Window layouts. Users, create a single layout (a list of lists) and pass as a parameter to Window object, or call Window.Layout(layout)

```
AddRow(args=*<1 or N object>)
```

Parameter Descriptions:

Type

Name

Meaning

*args

List[Elements]

### AddRows

Loops through a list of lists of elements and adds each row, list, to the layout. This is NOT the best way to go about creating a window. Sending the entire layout at one time and passing it as a parameter to the Window call is better.

```
AddRows(rows)
```

Parameter Descriptions:

Type

Name

Meaning

List[List[Elements]]

rows

A list of a list of elements

### AlphaChannel

#### property: AlphaChannel

A property that changes the current alpha channel value (internal value)

Type

Name

Meaning

(float)

**return**

the current alpha channel setting according to self, not read directly from tkinter

### BringToFront

Brings this window to the top of all other windows (perhaps may not be brought before a window made to "stay on top")

```python
BringToFront()
```

### Close

Closes window. Users can safely call even if window has been destroyed. Should always call when done with a window so that resources are properly freed up within your thread.

```python
Close()
```

### CurrentLocation

Get the current location of the window's top left corner. Sometimes, depending on the environment, the value returned does not include the titlebar,etc A new option, more_accurate, can be used to get the theoretical upper leftmost corner of the window. The titlebar and menubar are crated by the OS. It gets really confusing when running in a webpage (repl, trinket) Thus, the values can appear top be "off" due to the sometimes unpredictable way the location is calculated. If without_titlebar is set then the location of the root x,y is used which should not include the titlebar but may be OS dependent.

```
CurrentLocation(more_accurate = False, without_titlebar = False)
```

Parameter Descriptions:

Type

Name

Meaning

bool

more_accurate

If True, will use the window's geometry to get the topmost location with titlebar, menubar taken into account

bool

without_titlebar

If True, return location of top left of main window area without the titlebar (may be OS dependent?)

Tuple[(int or None), (int or None)]

**RETURN**

The x and y location in tuple form (x,y)

### Disable

Disables window from taking any input from the user

```python
Disable()
```

### DisableDebugger

Disable the internal debugger. By default the debugger is ENABLED

```python
DisableDebugger()
```

### Disappear

Causes a window to "disappear" from the screen, but remain on the taskbar. It does this by turning the alpha channel to 0. NOTE that on some platforms alpha is not supported. The window will remain showing on these platforms. The Raspberry Pi for example does not have an alpha setting

```python
Disappear()
```

### Elem

Find element object associated with the provided key. THIS METHOD IS NO LONGER NEEDED to be called by the user

You can perform the same operation by writing this statement: element = window[key]

You can drop the entire "find_element" function name and use [ ] instead.

However, if you wish to perform a lookup without error checking, and don't have error popups turned off globally, you'll need to make this call so that you can disable error checks on this call.

find_element is yypically used in combination with a call to element's Update method (or any other element method!): window[key].update(new_value)

Versus the "old way" window.FindElement(key).Update(new_value)

This call can be abbreviated to any of these: find_element = FindElement == Element == Find With find_element being the PEP8 compliant call that should be used.

Rememeber that this call will return None if no match is found which may cause your code to crash if not checked for.

```
Elem(key, silent_on_error = False)
```

Parameter Descriptions:

Type

Name

Meaning

str or int or tuple or object

key

Used with window.find_element and with return values to uniquely identify this element

bool

silent_on_error

If True do not display popup nor print warning of key errors

Element or Error Element or None

**RETURN**

Return value can be: the Element that matches the supplied key if found; an Error Element if silent_on_error is False; None if silent_on_error True;

### Element

Find element object associated with the provided key. THIS METHOD IS NO LONGER NEEDED to be called by the user

You can perform the same operation by writing this statement: element = window[key]

You can drop the entire "find_element" function name and use [ ] instead.

However, if you wish to perform a lookup without error checking, and don't have error popups turned off globally, you'll need to make this call so that you can disable error checks on this call.

find_element is yypically used in combination with a call to element's Update method (or any other element method!): window[key].update(new_value)

Versus the "old way" window.FindElement(key).Update(new_value)

This call can be abbreviated to any of these: find_element = FindElement == Element == Find With find_element being the PEP8 compliant call that should be used.

Rememeber that this call will return None if no match is found which may cause your code to crash if not checked for.

```
Element(key, silent_on_error = False)
```

Parameter Descriptions:

Type

Name

Meaning

str or int or tuple or object

key

Used with window.find_element and with return values to uniquely identify this element

bool

silent_on_error

If True do not display popup nor print warning of key errors

Element or Error Element or None

**RETURN**

Return value can be: the Element that matches the supplied key if found; an Error Element if silent_on_error is False; None if silent_on_error True;

### Enable

Re-enables window to take user input after having it be Disabled previously

```python
Enable()
```

### EnableDebugger

Enables the internal debugger. By default, the debugger IS enabled

```python
EnableDebugger()
```

### Fill

Fill in elements that are input fields with data based on a 'values dictionary'

```
Fill(values_dict)
```

Parameter Descriptions:

Type

Name

Meaning

(Dict[Any, Any]) - {Element_key : value}

values_dict

pairs

(Window)

**RETURN**

returns self so can be chained with other methods

### Finalize

Use this method to cause your layout to built into a real tkinter window. In reality this method is like Read(timeout=0). It doesn't block and uses your layout to create tkinter widgets to represent the elements. Lots of action!

`Finalize()`

Type

Name

Meaning

(Window)

**return**

Returns 'self' so that method "Chaining" can happen (read up about it as it's very cool!)

### Find

Find element object associated with the provided key. THIS METHOD IS NO LONGER NEEDED to be called by the user

You can perform the same operation by writing this statement: element = window[key]

You can drop the entire "find_element" function name and use [ ] instead.

However, if you wish to perform a lookup without error checking, and don't have error popups turned off globally, you'll need to make this call so that you can disable error checks on this call.

find_element is yypically used in combination with a call to element's Update method (or any other element method!): window[key].update(new_value)

Versus the "old way" window.FindElement(key).Update(new_value)

This call can be abbreviated to any of these: find_element = FindElement == Element == Find With find_element being the PEP8 compliant call that should be used.

Rememeber that this call will return None if no match is found which may cause your code to crash if not checked for.

```
Find(key, silent_on_error = False)
```

Parameter Descriptions:

Type

Name

Meaning

str or int or tuple or object

key

Used with window.find_element and with return values to uniquely identify this element

bool

silent_on_error

If True do not display popup nor print warning of key errors

Element or Error Element or None

**RETURN**

Return value can be: the Element that matches the supplied key if found; an Error Element if silent_on_error is False; None if silent_on_error True;

### FindElement

**Warning** This call will eventually be depricated. **

It is suggested that you modify your code to use the recommended window[key] lookup or the PEP8 compliant window.find_element(key)

For now, you'll only see a message printed and the call will continue to funcation as before.

```
FindElement(key, silent_on_error = False)
```

Parameter Descriptions:

Type

Name

Meaning

str or int or tuple or object

key

Used with window.find_element and with return values to uniquely identify this element

bool

silent_on_error

If True do not display popup nor print warning of key errors

Element or Error Element or None

**RETURN**

Return value can be: the Element that matches the supplied key if found; an Error Element if silent_on_error is False; None if silent_on_error True;

### FindElementWithFocus

Returns the Element that currently has focus as reported by tkinter. If no element is found None is returned!

`FindElementWithFocus()`

Type

Name

Meaning

Element

None

**return**

### GetScreenDimensions

Get the screen dimensions. NOTE - you must have a window already open for this to work (blame tkinter not me)

`GetScreenDimensions()`

Type

Name

Meaning

Tuple[None, None]

Tuple[width, height]

**return**

### GrabAnyWhereOff

Turns off Grab Anywhere functionality AFTER a window has been created. Don't try on a window that's not yet been Finalized or Read.

```python
GrabAnyWhereOff()
```

### GrabAnyWhereOn

Turns on Grab Anywhere functionality AFTER a window has been created. Don't try on a window that's not yet been Finalized or Read.

```python
GrabAnyWhereOn()
```

### Hide

Hides the window from the screen and the task bar

```python
Hide()
```

### Layout

Second of two preferred ways of telling a Window what its layout is. The other way is to pass the layout as a parameter to Window object. The parameter method is the currently preferred method. This call to Layout has been removed from examples contained in documents and in the Demo Programs. Trying to remove this call from history and replace with sending as a parameter to Window.

```
Layout(rows)
```

Parameter Descriptions:

Type

Name

Meaning

List[List[Elements]]

rows

Your entire layout

(Window)

**RETURN**

self so that you can chain method calls

### LoadFromDisk

Restore values from a previous call to SaveToDisk which saves the returned values dictionary in Pickle format

```
LoadFromDisk(filename)
```

Parameter Descriptions:

Type

Name

Meaning

str

filename

Pickle Filename to load

### Maximize

Maximize the window. This is done differently on a windows system versus a linux or mac one. For non-Windows the root attribute '-fullscreen' is set to True. For Windows the "root" state is changed to "zoomed" The reason for the difference is the title bar is removed in some cases when using fullscreen option

```python
Maximize()
```

### Minimize

Minimize this window to the task bar

```python
Minimize()
```

### Move

Move the upper left corner of this window to the x,y coordinates provided

```
Move(x, y)
```

Parameter Descriptions:

Type

Name

Meaning

int

x

x coordinate in pixels

int

y

y coordinate in pixels

### Normal

Restore a window to a non-maximized state. Does different things depending on platform. See Maximize for more.

```python
Normal()
```

### Read

THE biggest deal method in the Window class! This is how you get all of your data from your Window. Pass in a timeout (in milliseconds) to wait for a maximum of timeout milliseconds. Will return timeout_key if no other GUI events happen first.

```
Read(timeout = None,
    timeout_key = "__TIMEOUT__",
    close = False)
```

Parameter Descriptions:

Type

Name

Meaning

int

timeout

Milliseconds to wait until the Read will return IF no other GUI events happen first

Any

timeout_key

The value that will be returned from the call if the timer expired

bool

close

if True the window will be closed prior to returning

Tuple[(Any), Dict[Any, Any], List[Any], None]

**RETURN**

(event, values)

### Reappear

Causes a window previously made to "Disappear" (using that method). Does this by restoring the alpha channel

```python
Reappear()
```

### Refresh

Refreshes the window by calling tkroot.update(). Can sometimes get away with a refresh instead of a Read. Use this call when you want something to appear in your Window immediately (as soon as this function is called). If you change an element in a window, your change will not be visible until the next call to Window.read or a call to Window.refresh()

`Refresh()`

Type

Name

Meaning

(Window)

**return**

`self` so that method calls can be easily "chained"

### SaveToDisk

Saves the values contained in each of the input areas of the form. Basically saves what would be returned from a call to Read. It takes these results and saves them to disk using pickle. Note that every element in your layout that is to be saved must have a key assigned to it.

```
SaveToDisk(filename)
```

Parameter Descriptions:

Type

Name

Meaning

str

filename

Filename to save the values to in pickled form

### SendToBack

Pushes this window to the bottom of the stack of windows. It is the opposite of BringToFront

```python
SendToBack()
```

### SetAlpha

Sets the Alpha Channel for a window. Values are between 0 and 1 where 0 is completely transparent

```
SetAlpha(alpha)
```

Parameter Descriptions:

Type

Name

Meaning

float

alpha

0 to 1. 0 is completely transparent. 1 is completely visible and solid (can't see through)

### SetIcon

Changes the icon that is shown on the title bar and on the task bar. NOTE - The file type is IMPORTANT and depends on the OS! Can pass in: * filename which must be a .ICO icon file for windows, PNG file for Linux * bytes object * BASE64 encoded file held in a variable

```
SetIcon(icon = None, pngbase64 = None)
```

Parameter Descriptions:

Type

Name

Meaning

str

icon

Filename or bytes object

bytes

pngbase64

Base64 encoded image

### SetTransparentColor

Set the color that will be transparent in your window. Areas with this color will be SEE THROUGH.

```
SetTransparentColor(color)
```

Parameter Descriptions:

Type

Name

Meaning

str

color

Color string that defines the transparent color

### Size

#### property: Size

Return the current size of the window in pixels

Type

Name

Meaning

Tuple[(int), (int)] or Tuple[None, None]

**return**

(width, height) of the window

### UnHide

Used to bring back a window that was previously hidden using the Hide method

```python
UnHide()
```

### VisibilityChanged

When making an element in a column or someplace that has a scrollbar, then you'll want to call this function prior to the column's contents_changed() method.

```python
VisibilityChanged()
```

[Back](./_Elements)
