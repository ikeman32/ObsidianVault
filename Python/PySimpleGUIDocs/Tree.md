# Tree
```
Tree Element - Presents data in a tree-like manner, much like a file/folder browser.  Uses the TreeData class
to hold the user's data and pass to the element for display.
```

```
Tree(data = None,
    headings = None,
    visible_column_map = None,
    col_widths = None,
    col0_width = 10,
    col0_heading = "",
    def_col_width = 10,
    auto_size_columns = True,
    max_col_width = 20,
    select_mode = None,
    show_expanded = False,
    change_submits = False,
    enable_events = False,
    font = None,
    justification = "right",
    text_color = None,
    border_width = None,
    background_color = None,
    selected_row_colors = (None, None),
    header_text_color = None,
    header_background_color = None,
    header_font = None,
    header_border_width = None,
    header_relief = None,
    num_rows = None,
    sbar_trough_color = None,
    sbar_background_color = None,
    sbar_arrow_color = None,
    sbar_width = None,
    sbar_arrow_width = None,
    sbar_frame_color = None,
    sbar_relief = None,
    row_height = None,
    vertical_scroll_only = True,
    hide_vertical_scroll = False,
    pad = None,
    p = None,
    key = None,
    k = None,
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

TreeData

data

The data represented using a PySimpleGUI provided TreeData class

List[str]

headings

List of individual headings for each column

List[bool]

visible_column_map

Determines if a column should be visible. If left empty, all columns will be shown

List[int]

col_widths

List of column widths so that individual column widths can be controlled

int

col0_width

Size of Column 0 which is where the row numbers will be optionally shown

str

col0_heading

Text to be shown in the header for the left-most column

int

def_col_width

default column width

bool

auto_size_columns

if True, the size of a column is determined using the contents of the column

int

max_col_width

the maximum size a column can be

enum

select_mode

Use same values as found on Table Element. Valid values include: TABLE_SELECT_MODE_NONE TABLE_SELECT_MODE_BROWSE TABLE_SELECT_MODE_EXTENDED

bool

show_expanded

if True then the tree will be initially shown with all nodes completely expanded

bool

change_submits

DO NOT USE. Only listed for backwards compat - Use enable_events instead

bool

enable_events

Turns on the element specific events. Tree events happen when row is clicked

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

str

justification

'left', 'right', 'center' are valid choices

str

text_color

color of the text

int

border_width

Border width/depth in pixels

str

background_color

color of background

str or (str, str)

selected_row_colors

Sets the text color and background color for a selected row. Same format as button colors - tuple ('red', 'yellow') or string 'red on yellow'. Defaults to theme's button color

str

header_text_color

sets the text color for the header

str

header_background_color

sets the background color for the header

(str or (str, int[, str]) or None)

header_font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

(int or None)

header_border_width

Border width for the header portion

(str or None)

header_relief

Relief style for the header. Values are same as other elements that use relief. RELIEF_RAISED RELIEF_SUNKEN RELIEF_FLAT RELIEF_RIDGE RELIEF_GROOVE RELIEF_SOLID

int

num_rows

The number of rows of the table to display at a time

int

row_height

height of a single row in pixels

bool

vertical_scroll_only

if True only the vertical scrollbar will be visible

bool

hide_vertical_scroll

if True vertical scrollbar will be hidden

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

List[List[str] or str]]

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

Any

metadata

User metadata that can be set to ANYTHING

### add_treeview_data

Not a user function. Recursive method that inserts tree data into the tkinter treeview widget.

```
add_treeview_data(node)
```

Parameter Descriptions:

Type

Name

Meaning

TreeData

node

The node to insert. Will insert all nodes from starting point downward, recursively

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

Changes some of the settings for the Tree Element. Must call??`Window.Read`??or??`Window.Finalize`??prior

Changes will not be visible in your window until you call window.read or window.refresh.

If you change visibility, your element may MOVE. If you want it to remain stationary, use the "layout helper" function "pin" to ensure your element is "pinned" to that location in your layout so that it returns there when made visible.

```
update(values = None,
    key = None,
    value = None,
    text = None,
    icon = None,
    visible = None)
```

Parameter Descriptions:

Type

Name

Meaning

TreeData

values

Representation of the tree

str or int or tuple or object

key

identifies a particular item in tree to update

Any

value

sets the node identified by key to a particular value

str

text

sets the node identified by key to this string

bytes or str

icon

can be either a base64 icon or a filename for the icon

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

Changes some of the settings for the Tree Element. Must call??`Window.Read`??or??`Window.Finalize`??prior

Changes will not be visible in your window until you call window.read or window.refresh.

If you change visibility, your element may MOVE. If you want it to remain stationary, use the "layout helper" function "pin" to ensure your element is "pinned" to that location in your layout so that it returns there when made visible.

```
Update(values = None,
    key = None,
    value = None,
    text = None,
    icon = None,
    visible = None)
```

Parameter Descriptions:

Type

Name

Meaning

TreeData

values

Representation of the tree

str or int or tuple or object

key

identifies a particular item in tree to update

Any

value

sets the node identified by key to a particular value

str

text

sets the node identified by key to this string

bytes or str

icon

can be either a base64 icon or a filename for the icon

bool

visible

control visibility of element

[Back](./_Elements)
