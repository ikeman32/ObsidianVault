# Image
```
Image Element - show an image in the window. Should be a GIF or a PNG only
```

```
Image(source = None,
    filename = None,
    data = None,
    background_color = None,
    size = (None, None),
    s = (None, None),
    pad = None,
    p = None,
    key = None,
    k = None,
    tooltip = None,
    subsample = None,
    right_click_menu = None,
    expand_x = False,
    expand_y = False,
    visible = True,
    enable_events = False,
    metadata = None)
```

Parameter Descriptions:

Type

Name

Meaning

str or bytes or None

source

A filename or a base64 bytes. Will automatically detect the type and fill in filename or data for you.

str or None

filename

image filename if there is a button image. GIFs and PNGs only.

bytes or str or None

data

Raw or Base64 representation of the image to put on button. Choose either filename or data

background_color

color of background

(int, int)

size

(width, height) size of image in pixels

(int, int) or (None, None) or int

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

str or int or tuple or object

key

Used with window.find_element and with return values to uniquely identify this element to uniquely identify this element

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

str

tooltip

text, that will appear when mouse hovers over the element

int

subsample

amount to reduce the size of the image. Divides the size by this number. 2=1/2, 3=1/3, 4=1/4, etc

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

set visibility state of the element

bool

enable_events

Turns on the element specific events. For an Image element, the event is "image clicked"

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

Changes some of the settings for the Image Element. Must call `Window.Read` or `Window.Finalize` prior. To clear an image that's been displayed, call with NONE of the options set. A blank update call will delete the previously shown image.

Changes will not be visible in your window until you call window.read or window.refresh.

If you change visibility, your element may MOVE. If you want it to remain stationary, use the "layout helper" function "pin" to ensure your element is "pinned" to that location in your layout so that it returns there when made visible.

```
update(source = None,
    filename = None,
    data = None,
    size = (None, None),
    subsample = None,
    visible = None)
```

Parameter Descriptions:

Type

Name

Meaning

str or bytes or None

source

A filename or a base64 bytes. Will automatically detect the type and fill in filename or data for you.

str

filename

filename to the new image to display.

str or tkPhotoImage

data

Base64 encoded string OR a tk.PhotoImage object

Tuple[int,int]

size

(width, height) size of image in pixels

int

subsample

amount to reduce the size of the image. Divides the size by this number. 2=1/2, 3=1/3, 4=1/4, etc

bool

visible

control visibility of element

### update_animation

Show an Animated GIF. Call the function as often as you like. The function will determine when to show the next frame and will automatically advance to the next frame at the right time. NOTE - does NOT perform a sleep call to delay

```
update_animation(source, time_between_frames = 0)
```

Parameter Descriptions:

Type

Name

Meaning

str or bytes or None

source

Filename or Base64 encoded string containing Animated GIF

int

time_between_frames

Number of milliseconds to wait between showing frames

### update_animation_no_buffering

Show an Animated GIF. Call the function as often as you like. The function will determine when to show the next frame and will automatically advance to the next frame at the right time. NOTE - does NOT perform a sleep call to delay

```
update_animation_no_buffering(source, time_between_frames = 0)
```

Parameter Descriptions:

Type

Name

Meaning

str or bytes

source

Filename or Base64 encoded string containing Animated GIF

int

time_between_frames

Number of milliseconds to wait between showing frames

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

Changes some of the settings for the Image Element. Must call `Window.Read` or `Window.Finalize` prior. To clear an image that's been displayed, call with NONE of the options set. A blank update call will delete the previously shown image.

Changes will not be visible in your window until you call window.read or window.refresh.

If you change visibility, your element may MOVE. If you want it to remain stationary, use the "layout helper" function "pin" to ensure your element is "pinned" to that location in your layout so that it returns there when made visible.

```
Update(source = None,
    filename = None,
    data = None,
    size = (None, None),
    subsample = None,
    visible = None)
```

Parameter Descriptions:

Type

Name

Meaning

str or bytes or None

source

A filename or a base64 bytes. Will automatically detect the type and fill in filename or data for you.

str

filename

filename to the new image to display.

str or tkPhotoImage

data

Base64 encoded string OR a tk.PhotoImage object

Tuple[int,int]

size

(width, height) size of image in pixels

int

subsample

amount to reduce the size of the image. Divides the size by this number. 2=1/2, 3=1/3, 4=1/4, etc

bool

visible

control visibility of element

### UpdateAnimation

Show an Animated GIF. Call the function as often as you like. The function will determine when to show the next frame and will automatically advance to the next frame at the right time. NOTE - does NOT perform a sleep call to delay

```
UpdateAnimation(source, time_between_frames = 0)
```

Parameter Descriptions:

Type

Name

Meaning

str or bytes or None

source

Filename or Base64 encoded string containing Animated GIF

int

time_between_frames

Number of milliseconds to wait between showing frames

[Back](./_Elements)
