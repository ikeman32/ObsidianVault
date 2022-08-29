# Tab Group
```
TabGroup Element groups together your tabs into the group of tabs you see displayed in your window
```

```
TabGroup(layout,
    tab_location = None,
    title_color = None,
    tab_background_color = None,
    selected_title_color = None,
    selected_background_color = None,
    background_color = None,
    focus_color = None,
    font = None,
    change_submits = False,
    enable_events = False,
    pad = None,
    p = None,
    border_width = None,
    tab_border_width = None,
    theme = None,
    key = None,
    k = None,
    size = (None, None),
    s = (None, None),
    tooltip = None,
    right_click_menu = None,
    expand_x = False,
    expand_y = False,
    visible = True,
    metadata = None)
```

Parameter Descriptions:

Type

Name

Meaning

List[List[Tab]]

layout

Layout of Tabs. Different than normal layouts. ALL Tabs should be on first row

str

tab_location

location that tabs will be displayed. Choices are left, right, top, bottom, lefttop, leftbottom, righttop, rightbottom, bottomleft, bottomright, topleft, topright

str

title_color

color of text on tabs

str

tab_background_color

color of all tabs that are not selected

str

selected_title_color

color of tab text when it is selected

str

selected_background_color

color of tab when it is selected

str

background_color

color of background area that tabs are located on

str

focus_color

color of focus indicator on the tabs

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

change_submits

* DEPRICATED DO NOT USE. Use `enable_events` instead

bool

enable_events

If True then switching tabs will generate an Event

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

int

border_width

width of border around element in pixels

int

tab_border_width

width of border around the tabs

enum

theme

DEPRICATED - You can only specify themes using set options or when window is created. It's not possible to do it on an element basis

str or int or tuple or object

key

Value that uniquely identifies this element from all other elements. Used when Finding an element or in return values. Must be unique to the window

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

(intorNone, intorNone)

size

(width, height) w=pixels-wide, h=pixels-high. Either item in tuple can be None to indicate use the computed value and set only 1 direction

(intorNone, intorNone)

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

str

tooltip

text, that will appear when mouse hovers over the element

List[List[ List[str] or str ]]

right_click_menu

A list of lists of Menu items to show when this element is right clicked. See user docs for exact format.

bool

expand_x

If True the element will automatically expand in the X direction to fill available space

bool

expand_y

If True the element will automatically expand in the Y direction to fill available space

bool

visible

DEPRECATED - Should you need to control visiblity for the TabGroup as a whole, place it into a Column element

Any

metadata

User metadata that can be set to ANYTHING

### add_tab

Add a new tab to an existing TabGroup This call was written so that tabs can be added at runtime as your user performs operations. Your Window should already be created and finalized.

```
add_tab(tab_element)
```

Parameter Descriptions:

Type

Name

Meaning

Tab

tab_element

A Tab Element that has a layout in it

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

### find_key_from_tab_name

Searches through the layout to find the key that matches the text on the tab. Implies names should be unique

```
find_key_from_tab_name(tab_name)
```

Parameter Descriptions:

Type

Name

Meaning

str

tab_name

name of a tab

key or None

**RETURN**

Returns the key or None if no key found

### get

Returns the current value for the Tab Group, which will be the currently selected tab's KEY or the text on the tab if no key is defined. Returns None if an error occurs. Note that this is exactly the same data that would be returned from a call to Window.Read. Are you sure you are using this method correctly?

`get()`

Type

Name

Meaning

Any

None

**return**

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

### FindKeyFromTabName

Searches through the layout to find the key that matches the text on the tab. Implies names should be unique

```
FindKeyFromTabName(tab_name)
```

Parameter Descriptions:

Type

Name

Meaning

str

tab_name

name of a tab

key or None

**RETURN**

Returns the key or None if no key found

### Get

Returns the current value for the Tab Group, which will be the currently selected tab's KEY or the text on the tab if no key is defined. Returns None if an error occurs. Note that this is exactly the same data that would be returned from a call to Window.Read. Are you sure you are using this method correctly?

`Get()`

Type

Name

Meaning

Any

None

**return**

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

[Back](./_Elements)
