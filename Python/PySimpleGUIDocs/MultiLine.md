# MultiLine
```
Multiline Element - Display and/or read multiple lines of text.  This is both an input and output element.
Other PySimpleGUI ports have a separate MultilineInput and MultilineOutput elements.  May want to split this
one up in the future too.
```

```
Multiline(default_text = "",
    enter_submits = False,
    disabled = False,
    autoscroll = False,
    border_width = None,
    size = (None, None),
    s = (None, None),
    auto_size_text = None,
    background_color = None,
    text_color = None,
    horizontal_scroll = False,
    change_submits = False,
    enable_events = False,
    do_not_clear = True,
    key = None,
    k = None,
    write_only = False,
    auto_refresh = False,
    reroute_stdout = False,
    reroute_stderr = False,
    reroute_cprint = False,
    echo_stdout_stderr = False,
    focus = False,
    font = None,
    pad = None,
    p = None,
    tooltip = None,
    justification = None,
    no_scrollbar = False,
    wrap_lines = None,
    sbar_trough_color = None,
    sbar_background_color = None,
    sbar_arrow_color = None,
    sbar_width = None,
    sbar_arrow_width = None,
    sbar_frame_color = None,
    sbar_relief = None,
    expand_x = False,
    expand_y = False,
    rstrip = True,
    right_click_menu = None,
    visible = True,
    metadata = None)
```

Parameter Descriptions:

Type

Name

Meaning

Any

default_text

Initial text to show

bool

enter_submits

if True, the Window.Read call will return is enter key is pressed in this element

bool

disabled

set disable state

bool

autoscroll

If True the contents of the element will automatically scroll as more data added to the end

int

border_width

width of border around element in pixels

(int, int) or (None, None) or int

size

(w, h) w=characters-wide, h=rows-high. If an int instead of a tuple is supplied, then height is auto-set to 1

(int, int) or (None, None) or int

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

bool

auto_size_text

if True will size the element to match the length of the text

str

background_color

color of background

str

text_color

color of the text

bool

horizontal_scroll

Controls if a horizontal scrollbar should be shown. If True a horizontal scrollbar will be shown in addition to vertical

bool

change_submits

DO NOT USE. Only listed for backwards compat - Use enable_events instead

bool

enable_events

Turns on the element specific events. Spin events happen when an item changes

bool

do_not_clear

if False the element will be cleared any time the Window.Read call returns

str or int or tuple or object

key

Used with window.find_element and with return values to uniquely identify this element to uniquely identify this element

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

bool

write_only

If True then no entry will be added to the values dictionary when the window is read

bool

auto_refresh

If True then anytime the element is updated, the window will be refreshed so that the change is immediately displayed

bool

reroute_stdout

If True then all output to stdout will be output to this element

bool

reroute_stderr

If True then all output to stderr will be output to this element

bool

reroute_cprint

If True your cprint calls will output to this element. It's the same as you calling cprint_set_output_destination

bool

echo_stdout_stderr

If True then output to stdout and stderr will be output to this element AND also to the normal console location

bool

focus

if True initial focus will go to this element

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

str

tooltip

text, that will appear when mouse hovers over the element

str

justification

text justification. left, right, center. Can use single characters l, r, c.

bool

no_scrollbar

If False then a vertical scrollbar will be shown (the default)

bool

wrap_lines

If True, the lines will be wrapped automatically. Other parms affect this setting, but this one will override them all. Default is it does nothing and uses previous settings for wrapping.

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

bool

expand_x

If True the element will automatically expand in the X direction to fill available space

bool

expand_y

If True the element will automatically expand in the Y direction to fill available space

bool

rstrip

If True the value returned in will have whitespace stripped from the right side

List[List[ List[str] or str ]]

right_click_menu

A list of lists of Menu items to show when this element is right clicked. See user docs for exact format.

bool

visible

set visibility state of the element

Any

metadata

User metadata that can be set to ANYTHING

### bind

Used to add tkinter events to an Element. The tkinter specific data is in the Element's member variable user_bind_event

```
bind(bind_string,
    key_modifier,
    propagate = True)
```

Parameter Descriptions:

Type

Name

Meaning

str

bind_string

The string tkinter expected in its bind function

str

key_modifier

Additional data to be added to the element's key when event is returned

bool

propagate

If True then tkinter will be told to propagate the event to the element

### block_focus

Enable or disable the element from getting focus by using the keyboard. If the block parameter is True, then this element will not be given focus by using the keyboard to go from one element to another. You CAN click on the element and utilize it.

```
block_focus(block = True)
```

Parameter Descriptions:

Type

Name

Meaning

bool

block

if True the element will not get focus via the keyboard

### expand

Causes the Element to expand to fill available space in the X and Y directions. Can specify which or both directions

```
expand(expand_x = False,
    expand_y = False,
    expand_row = True)
```

Parameter Descriptions:

Type

Name

Meaning

bool

expand_x

If True Element will expand in the Horizontal directions

bool

expand_y

If True Element will expand in the Vertical directions

bool

expand_row

If True the row containing the element will also expand. Without this your element is "trapped" within the row

### get

Return current contents of the Multiline Element

`get()`

Type

Name

Meaning

(str)

**return**

current contents of the Multiline Element (used as an input type of Multiline

### get_next_focus

Gets the next element that should get focus after this element.

`get_next_focus()`

Type

Name

Meaning

(Element)

**return**

Element that will get focus after this one

### get_previous_focus

Gets the element that should get focus previous to this element.

`get_previous_focus()`

Type

Name

Meaning

(Element)

**return**

Element that should get the focus before this one

### get_size

Return the size of an element in Pixels. Care must be taken as some elements use characters to specify their size but will return pixels when calling this get_size method.

`get_size()`

Type

Name

Meaning

(int, int)

**return**

width and height of the element

### grab_anywhere_exclude

Excludes this element from being used by the grab_anywhere feature Handy for elements like a Graph element when dragging is enabled. You want the Graph element to get the drag events instead of the window dragging.

```python
grab_anywhere_exclude()
```

### grab_anywhere_include

Includes this element in the grab_anywhere feature This will allow you to make a Multline element drag a window for example

```python
grab_anywhere_include()
```

### hide_row

Hide the entire row an Element is located on. Use this if you must have all space removed when you are hiding an element, including the row container

```python
hide_row()
```

### print

Print like Python normally prints except route the output to a multiline element and also add colors if desired

colors -(str, str) or str. A combined text/background color definition in a single parameter

There are also "aliases" for text_color, background_color and colors (t, b, c) t - An alias for color of the text (makes for shorter calls) b - An alias for the background_color parameter c - (str, str) - "shorthand" way of specifying color. (foreground, backgrouned) c - str - can also be a string of the format "foreground on background" ("white on red")

With the aliases it's possible to write the same print but in more compact ways: cprint('This will print white text on red background', c=('white', 'red')) cprint('This will print white text on red background', c='white on red') cprint('This will print white text on red background', text_color='white', background_color='red') cprint('This will print white text on red background', t='white', b='red')

```
print(args=*<1 or N object>,
    end = None,
    sep = None,
    text_color = None,
    background_color = None,
    justification = None,
    font = None,
    colors = None,
    t = None,
    b = None,
    c = None,
    autoscroll = True)
```

Parameter Descriptions:

Type

Name

Meaning

Any

args

The arguments to print

str

end

The end char to use just like print uses

str

sep

The separation character like print uses

str

text_color

The color of the text

str

background_color

The background color of the line

str

justification

text justification. left, right, center. Can use single characters l, r, c. Sets only for this value, not entire element

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike for the args being printed

str or str, str

colors

Either a tuple or a string that has both the text and background colors. Or just the text color

str

t

Color of the text

str

b

The background color of the line

str or str, str

c

Either a tuple or a string that has both the text and background colors or just tex color (same as the color parm)

bool

autoscroll

If True the contents of the element will automatically scroll as more data added to the end

### reroute_stderr_to_here

Sends stderr to this element

```python
reroute_stderr_to_here()
```

### reroute_stdout_to_here

Sends stdout (prints) to this element

```python
reroute_stdout_to_here()
```

### restore_stderr

Restore a previously re-reouted stderr back to the original destination

```python
restore_stderr()
```

### restore_stdout

Restore a previously re-reouted stdout back to the original destination

```python
restore_stdout()
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

Metadata is an Element property that you can use at any time to hold any value

Type

Name

Meaning

(Any)

**return**

the current metadata value

### set_cursor

Sets the cursor for the current Element. "Cursor" is used in 2 different ways in this call. For the parameter "cursor" it's actually the mouse pointer. If you do not want any mouse pointer, then use the string "none" For the parameter "cursor_color" it's the color of the beam used when typing into an input element

```
set_cursor(cursor = None, cursor_color = None)
```

Parameter Descriptions:

Type

Name

Meaning

str

cursor

The tkinter cursor name

str

cursor_color

color to set the "cursor" to

### set_focus

Sets the current focus to be on this element

```
set_focus(force = False)
```

Parameter Descriptions:

Type

Name

Meaning

bool

force

if True will call focus_force otherwise calls focus_set

### set_size

Changes the size of an element to a specific size. It's possible to specify None for one of sizes so that only 1 of the element's dimensions are changed.

```
set_size(size = (None, None))
```

Parameter Descriptions:

Type

Name

Meaning

(int, int)

size

The size in characters, rows typically. In some cases they are pixels

### set_tooltip

Called by application to change the tooltip text for an Element. Normally invoked using the Element Object such as: window.Element('key').SetToolTip('New tip').

```
set_tooltip(tooltip_text)
```

Parameter Descriptions:

Type

Name

Meaning

str

tooltip_text

the text to show in tooltip.

### set_vscroll_position

Attempts to set the vertical scroll postition for an element's Widget

```
set_vscroll_position(percent_from_top)
```

Parameter Descriptions:

Type

Name

Meaning

float

percent_from_top

From 0 to 1.0, the percentage from the top to move scrollbar to

### unbind

Removes a previously bound tkinter event from an Element.

```
unbind(bind_string)
```

Parameter Descriptions:

Type

Name

Meaning

str

bind_string

The string tkinter expected in its bind function

### unhide_row

Unhides (makes visible again) the row container that the Element is located on. Note that it will re-appear at the bottom of the window / container, most likely.

```python
unhide_row()
```

### update

Changes some of the settings for the Multiline Element. Must call `Window.Read` or `Window.Finalize` prior

Changes will not be visible in your window until you call window.read or window.refresh.

If you change visibility, your element may MOVE. If you want it to remain stationary, use the "layout helper" function "pin" to ensure your element is "pinned" to that location in your layout so that it returns there when made visible.

```
update(value = None,
    disabled = None,
    append = False,
    font = None,
    text_color = None,
    background_color = None,
    text_color_for_value = None,
    background_color_for_value = None,
    visible = None,
    autoscroll = None,
    justification = None,
    font_for_value = None)
```

Parameter Descriptions:

Type

Name

Meaning

Any

value

new text to display

bool

disabled

disable or enable state of the element

bool

append

if True then new value will be added onto the end of the current value. if False then contents will be replaced.

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike for the entire element

str

text_color

color of the text

str

background_color

color of background

str

text_color_for_value

color of the new text being added (the value paramter)

str

background_color_for_value

color of the new background of the text being added (the value paramter)

bool

visible

set visibility state of the element

bool

autoscroll

if True then contents of element are scrolled down when new text is added to the end

str

justification

text justification. left, right, center. Can use single characters l, r, c. Sets only for this value, not entire element

str or (str, int)

font_for_value

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike for the value being updated

### visible

#### property: visible

Returns visibility state for the element. This is a READONLY property

Type

Name

Meaning

(bool)

**return**

Visibility state for element

### widget

#### property: widget

Returns tkinter widget for the element. This is a READONLY property. The implementation is that the Widget member variable is returned. This is a backward compatible addition

Type

Name

Meaning

(tkinter.Widget)

**return**

The element's underlying tkinter widget

---

### These are non-PEP8 Compliant Methods - do NOT use

The following methods are here for backwards compatibility reference. You will find there are PEP8 versions for each of these methods. The PEP8 versions will be all lower case and have underscores.

### Get

Return current contents of the Multiline Element

`Get()`

Type

Name

Meaning

(str)

**return**

current contents of the Multiline Element (used as an input type of Multiline

### SetFocus

Sets the current focus to be on this element

```
SetFocus(force = False)
```

Parameter Descriptions:

Type

Name

Meaning

bool

force

if True will call focus_force otherwise calls focus_set

### SetTooltip

Called by application to change the tooltip text for an Element. Normally invoked using the Element Object such as: window.Element('key').SetToolTip('New tip').

```
SetTooltip(tooltip_text)
```

Parameter Descriptions:

Type

Name

Meaning

str

tooltip_text

the text to show in tooltip.

### Update

Changes some of the settings for the Multiline Element. Must call `Window.Read` or `Window.Finalize` prior

Changes will not be visible in your window until you call window.read or window.refresh.

If you change visibility, your element may MOVE. If you want it to remain stationary, use the "layout helper" function "pin" to ensure your element is "pinned" to that location in your layout so that it returns there when made visible.

```
Update(value = None,
    disabled = None,
    append = False,
    font = None,
    text_color = None,
    background_color = None,
    text_color_for_value = None,
    background_color_for_value = None,
    visible = None,
    autoscroll = None,
    justification = None,
    font_for_value = None)
```

Parameter Descriptions:

Type

Name

Meaning

Any

value

new text to display

bool

disabled

disable or enable state of the element

bool

append

if True then new value will be added onto the end of the current value. if False then contents will be replaced.

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike for the entire element

str

text_color

color of the text

str

background_color

color of background

str

text_color_for_value

color of the new text being added (the value paramter)

str

background_color_for_value

color of the new background of the text being added (the value paramter)

bool

visible

set visibility state of the element

bool

autoscroll

if True then contents of element are scrolled down when new text is added to the end

str

justification

text justification. left, right, center. Can use single characters l, r, c. Sets only for this value, not entire element

str or (str, int)

font_for_value

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike for the value being updated

[Back](./_Elements)
