# Button Menu
```
The Button Menu Element.  Creates a button that when clicked will show a menu similar to right click menu
```

```
ButtonMenu(button_text,
    menu_def,
    tooltip = None,
    disabled = False,
    image_source = None,
    image_filename = None,
    image_data = None,
    image_size = (None, None),
    image_subsample = None,
    border_width = None,
    size = (None, None),
    s = (None, None),
    auto_size_button = None,
    button_color = None,
    text_color = None,
    background_color = None,
    disabled_text_color = None,
    font = None,
    item_font = None,
    pad = None,
    p = None,
    expand_x = False,
    expand_y = False,
    key = None,
    k = None,
    tearoff = False,
    visible = True,
    metadata = None)
```

Parameter Descriptions:

Type

Name

Meaning

str

button_text

Text to be displayed on the button

List[List[str]]

menu_def

A list of lists of Menu items to show when this element is clicked. See docs for format as they are the same for all menu types

str

tooltip

text, that will appear when mouse hovers over the element

bool

disabled

If True button will be created disabled

(str or bytes)

image_source

Image to place on button. Use INSTEAD of the image_filename and image_data. Unifies these into 1 easier to use parm

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

int

border_width

width of border around button in pixels

(int, int) or (None, None) or int

size

(w, h) w=characters-wide, h=rows-high. If an int instead of a tuple is supplied, then height is auto-set to 1

(int, int) or (None, None) or int

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

bool

auto_size_button

if True the button size is sized to fit the text

(str, str) or str

button_color

of button. Easy to remember which is which if you say "ON" between colors. "red" on "green"

str

background_color

color of the background

str

text_color

element's text color. Can be in #RRGGBB format or a color name "black"

str

disabled_text_color

color to use for text when item is disabled. Can be in #RRGGBB format or a color name "black"

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

(str or (str, int[, str]) or None)

item_font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike, for the menu items

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

bool

expand_x

If True the element will automatically expand in the X direction to fill available space

bool

expand_y

If True the element will automatically expand in the Y direction to fill available space

str or int or tuple or object

key

Used with window.find_element and with return values to uniquely identify this element to uniquely identify this element

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

bool

tearoff

Determines if menus should allow them to be torn off

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

### unhide_row

Unhides (makes visible again) the row container that the Element is located on. Note that it will re-appear at the bottom of the window / container, most likely.

```python
unhide_row()
```

### update

Changes some of the settings for the ButtonMenu Element. Must call `Window.Read` or `Window.Finalize` prior

Changes will not be visible in your window until you call window.read or window.refresh.

If you change visibility, your element may MOVE. If you want it to remain stationary, use the "layout helper" function "pin" to ensure your element is "pinned" to that location in your layout so that it returns there when made visible.

```
update(menu_definition = None,
    visible = None,
    image_source = None,
    image_size = (None, None),
    image_subsample = None,
    button_text = None)
```

Parameter Descriptions:

Type

Name

Meaning

List[List]

menu_definition

(New menu definition (in menu definition format)

bool

visible

control visibility of element

(str or bytes)

image_source

new image if image is to be changed. Can be a filename or a base64 encoded byte-string

(int, int)

image_size

Size of the image in pixels (width, height)

int

image_subsample

amount to reduce the size of the image. Divides the size by this number. 2=1/2, 3=1/3, 4=1/4, etc

str

button_text

Text to be shown on the button

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

### Click

Generates a click of the button as if the user clicked the button Calls the tkinter invoke method for the button

```python
Click()
```

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

Changes some of the settings for the ButtonMenu Element. Must call `Window.Read` or `Window.Finalize` prior

Changes will not be visible in your window until you call window.read or window.refresh.

If you change visibility, your element may MOVE. If you want it to remain stationary, use the "layout helper" function "pin" to ensure your element is "pinned" to that location in your layout so that it returns there when made visible.

```
Update(menu_definition = None,
    visible = None,
    image_source = None,
    image_size = (None, None),
    image_subsample = None,
    button_text = None)
```

Parameter Descriptions:

Type

Name

Meaning

List[List]

menu_definition

(New menu definition (in menu definition format)

bool

visible

control visibility of element

(str or bytes)

image_source

new image if image is to be changed. Can be a filename or a base64 encoded byte-string

(int, int)

image_size

Size of the image in pixels (width, height)

int

image_subsample

amount to reduce the size of the image. Divides the size by this number. 2=1/2, 3=1/3, 4=1/4, etc

str

button_text

Text to be shown on the button

[Back](./_Elements)
