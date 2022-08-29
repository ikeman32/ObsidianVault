# Input
```
Display a single text input field.  Based on the tkinter Widget `Entry`
```

```
Input(default_text = "",
    size = (None, None),
    s = (None, None),
    disabled = False,
    password_char = "",
    justification = None,
    background_color = None,
    text_color = None,
    font = None,
    tooltip = None,
    border_width = None,
    change_submits = False,
    enable_events = False,
    do_not_clear = True,
    key = None,
    k = None,
    focus = False,
    pad = None,
    p = None,
    use_readonly_for_disable = True,
    readonly = False,
    disabled_readonly_background_color = None,
    disabled_readonly_text_color = None,
    expand_x = False,
    expand_y = False,
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

Text initially shown in the input box as a default value(Default value = ''). Will automatically be converted to string

(int, int) or (int, None) or int

size

w=characters-wide, h=rows-high. If an int is supplied rather than a tuple, then a tuple is created width=int supplied and heigh=1

(int, int) or (None, None) or int

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

bool

disabled

set disable state for element (Default = False)

char

password_char

Password character if this is a password field (Default value = '')

str

justification

justification for data display. Valid choices - left, right, center

str

background_color

color of background in one of the color formats

str

text_color

color of the text

(str or (str, int[, str]) or None)

font

specifies the font family, size. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

str

tooltip

text, that will appear when mouse hovers over the element

int

border_width

width of border around element in pixels

bool

change_submits

* DEPRICATED DO NOT USE. Use `enable_events` instead

bool

enable_events

If True then changes to this element are immediately reported as an event. Use this instead of change_submits (Default = False)

bool

do_not_clear

If False then the field will be set to blank after ANY event (button, any event) (Default = True)

str or int or tuple or object

key

Value that uniquely identifies this element from all other elements. Used when Finding an element or in return values. Must be unique to the window

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

bool

focus

Determines if initial focus should go to this element.

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element. Normally (horizontal pixels, vertical pixels) but can be split apart further into ((horizontal left, horizontal right), (vertical above, vertical below)). If int is given, then converted to tuple (int, int) with the value provided duplicated

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

bool

use_readonly_for_disable

If True (the default) tkinter state set to 'readonly'. Otherwise state set to 'disabled'

bool

readonly

If True tkinter state set to 'readonly'. Use this in place of use_readonly_for_disable as another way of achieving readonly. Note cannot set BOTH readonly and disabled as tkinter only supplies a single flag

str

disabled_readonly_background_color

If state is set to readonly or disabled, the color to use for the background

str

disabled_readonly_text_color

If state is set to readonly or disabled, the color to use for the text

bool

expand_x

If True the element will automatically expand in the X direction to fill available space

bool

expand_y

If True the element will automatically expand in the Y direction to fill available space

List[List[ List[str] or str ]]

right_click_menu

A list of lists of Menu items to show when this element is right clicked. See user docs for exact format.

bool

visible

set visibility state of the element (Default = True)

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

Read and return the current value of the input element. Must call `Window.Read` or `Window.Finalize` prior

`get()`

Type

Name

Meaning

(str)

**return**

current value of Input field or '' if error encountered

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

Changes some of the settings for the Input Element. Must call `Window.Read` or `Window.Finalize` prior. Changes will not be visible in your window until you call window.read or window.refresh.

If you change visibility, your element may MOVE. If you want it to remain stationary, use the "layout helper" function "pin" to ensure your element is "pinned" to that location in your layout so that it returns there when made visible.

```
update(value = None,
    disabled = None,
    select = None,
    visible = None,
    text_color = None,
    background_color = None,
    move_cursor_to = "end",
    password_char = None,
    paste = None,
    readonly = None)
```

Parameter Descriptions:

Type

Name

Meaning

str

value

new text to display as default text in Input field

bool

disabled

disable or enable state of the element (sets Entry Widget to readonly or normal)

bool

select

if True, then the text will be selected

bool

visible

change visibility of element

str

text_color

change color of text being typed

str

background_color

change color of the background

int or str

move_cursor_to

Moves the cursor to a particular offset. Defaults to 'end'

str

password_char

Password character if this is a password field

bool

paste

If True "Pastes" the value into the element rather than replacing the entire element. If anything is selected it is replaced. The text is inserted at the current cursor location.

bool

readonly

if True make element readonly (user cannot change any choices). Enables the element if either choice are made.

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

Read and return the current value of the input element. Must call `Window.Read` or `Window.Finalize` prior

`Get()`

Type

Name

Meaning

(str)

**return**

current value of Input field or '' if error encountered

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

Changes some of the settings for the Input Element. Must call `Window.Read` or `Window.Finalize` prior. Changes will not be visible in your window until you call window.read or window.refresh.

If you change visibility, your element may MOVE. If you want it to remain stationary, use the "layout helper" function "pin" to ensure your element is "pinned" to that location in your layout so that it returns there when made visible.

```
Update(value = None,
    disabled = None,
    select = None,
    visible = None,
    text_color = None,
    background_color = None,
    move_cursor_to = "end",
    password_char = None,
    paste = None,
    readonly = None)
```

Parameter Descriptions:

Type

Name

Meaning

str

value

new text to display as default text in Input field

bool

disabled

disable or enable state of the element (sets Entry Widget to readonly or normal)

bool

select

if True, then the text will be selected

bool

visible

change visibility of element

str

text_color

change color of text being typed

str

background_color

change color of the background

int or str

move_cursor_to

Moves the cursor to a particular offset. Defaults to 'end'

str

password_char

Password character if this is a password field

bool

paste

If True "Pastes" the value into the element rather than replacing the entire element. If anything is selected it is replaced. The text is inserted at the current cursor location.

bool

readonly

if True make element readonly (user cannot change any choices). Enables the element if either choice are made.

[Back](./_Elements)
