# Column
```
A container element that is used to create a layout within your window's layout
```

```
Column(layout,
    background_color = None,
    size = (None, None),
    s = (None, None),
    size_subsample_width = 1,
    size_subsample_height = 2,
    pad = None,
    p = None,
    scrollable = False,
    vertical_scroll_only = False,
    right_click_menu = None,
    key = None,
    k = None,
    visible = True,
    justification = None,
    element_justification = None,
    vertical_alignment = None,
    grab = None,
    expand_x = None,
    expand_y = None,
    metadata = None,
    sbar_trough_color = None,
    sbar_background_color = None,
    sbar_arrow_color = None,
    sbar_width = None,
    sbar_arrow_width = None,
    sbar_frame_color = None,
    sbar_relief = None)
```

Parameter Descriptions:

Type

Name

Meaning

List[List[Element]]

layout

Layout that will be shown in the Column container

str

background_color

color of background of entire Column

(int or None, int or None)

size

(width, height) size in pixels (doesn't work quite right, sometimes only 1 dimension is set by tkinter. Use a Sizer Element to help set sizes

(int or None, int or None)

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

float

size_subsample_width

Determines the size of a scrollable column width based on 1/size_subsample * required size. 1 = match the contents exactly, 2 = 1/2 contents size, 3 = 1/3. Can be a fraction to make larger than required.

float

size_subsample_height

Determines the size of a scrollable height based on 1/size_subsample * required size. 1 = match the contents exactly, 2 = 1/2 contents size, 3 = 1/3. Can be a fraction to make larger than required..

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

bool

scrollable

if True then scrollbars will be added to the column. If you update the contents of a scrollable column, be sure and call Column.contents_changed also

bool

vertical_scroll_only

if True then no horizontal scrollbar will be shown if a scrollable column

List[List[ List[str] or str ]]

right_click_menu

A list of lists of Menu items to show when this element is right clicked. See user docs for exact format.

str or int or tuple or object

key

Value that uniquely identifies this element from all other elements. Used when Finding an element or in return values. Must be unique to the window

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

bool

visible

set visibility state of the element

str

justification

set justification for the Column itself. Note entire row containing the Column will be affected

str

element_justification

All elements inside the Column will have this justification 'left', 'right', 'center' are valid values

str

vertical_alignment

Place the column at the 'top', 'center', 'bottom' of the row (can also use t,c,r). Defaults to no setting (tkinter decides)

bool

grab

If True can grab this element and move the window around. Default is False

bool

expand_x

If True the column will automatically expand in the X direction to fill available space

bool

expand_y

If True the column will automatically expand in the Y direction to fill available space

Any

metadata

User metadata that can be set to ANYTHING

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

### add_row

Not recommended user call. Used to add rows of Elements to the Column Element.

```
add_row(args=*<1 or N object>)
```

Parameter Descriptions:

Type

Name

Meaning

List[Element]

*args

The list of elements for this row

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

### contents_changed

When a scrollable column has part of its layout changed by making elements visible or invisible or the layout is extended for the Column, then this method needs to be called so that the new scroll area is computed to match the new contents.

```python
contents_changed()
```

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

### layout

Can use like the Window.Layout method, but it's better to use the layout parameter when creating

```
layout(rows)
```

Parameter Descriptions:

Type

Name

Meaning

List[List[Element]]

rows

The rows of Elements

(Column)

**RETURN**

Used for chaining

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

Changes some of the settings for the Column Element. Must call `Window.Read` or `Window.Finalize` prior

Changes will not be visible in your window until you call window.read or window.refresh.

If you change visibility, your element may MOVE. If you want it to remain stationary, use the "layout helper" function "pin" to ensure your element is "pinned" to that location in your layout so that it returns there when made visible.

```
update(visible = None)
```

Parameter Descriptions:

Type

Name

Meaning

bool

visible

control visibility of element

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

### AddRow

Not recommended user call. Used to add rows of Elements to the Column Element.

```
AddRow(args=*<1 or N object>)
```

Parameter Descriptions:

Type

Name

Meaning

List[Element]

*args

The list of elements for this row

### Layout

Can use like the Window.Layout method, but it's better to use the layout parameter when creating

```
Layout(rows)
```

Parameter Descriptions:

Type

Name

Meaning

List[List[Element]]

rows

The rows of Elements

(Column)

**RETURN**

Used for chaining

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

Changes some of the settings for the Column Element. Must call `Window.Read` or `Window.Finalize` prior

Changes will not be visible in your window until you call window.read or window.refresh.

If you change visibility, your element may MOVE. If you want it to remain stationary, use the "layout helper" function "pin" to ensure your element is "pinned" to that location in your layout so that it returns there when made visible.

```
Update(visible = None)
```

Parameter Descriptions:

Type

Name

Meaning

bool

visible

control visibility of element

[Back](./_Elements)
