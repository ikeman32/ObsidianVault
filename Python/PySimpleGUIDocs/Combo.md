# Combo
```
ComboBox Element - A combination of a single-line input and a drop-down menu. User can type in their own value or choose from list.
```

```
Combo(values,
    default_value = None,
    size = (None, None),
    s = (None, None),
    auto_size_text = None,
    background_color = None,
    text_color = None,
    button_background_color = None,
    button_arrow_color = None,
    bind_return_key = False,
    change_submits = False,
    enable_events = False,
    disabled = False,
    key = None,
    k = None,
    pad = None,
    p = None,
    expand_x = False,
    expand_y = False,
    tooltip = None,
    readonly = False,
    font = None,
    visible = True,
    metadata = None)
```

Parameter Descriptions:

Type

Name

Meaning

List[Any] or Tuple[Any]

values

values to choose. While displayed as text, the items returned are what the caller supplied, not text

Any

default_value

Choice to be displayed as initial value. Must match one of values variable contents

(int, int) or (None, None) or int

size

width, height. Width = characters-wide, height = NOTE it's the number of entries to show in the list. If an Int is passed rather than a tuple, then height is auto-set to 1 and width is value of the int

(int, int) or (None, None) or int

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

bool

auto_size_text

True if element should be the same size as the contents

str

background_color

color of background

str

text_color

color of the text

str

button_background_color

The color of the background of the button on the combo box

str

button_arrow_color

The color of the arrow on the button on the combo box

bool

bind_return_key

If True, then the return key will cause a the Combo to generate an event

bool

change_submits

DEPRICATED DO NOT USE. Use `enable_events` instead

bool

enable_events

Turns on the element specific events. Combo event is when a choice is made

bool

disabled

set disable state for element

str or int or tuple or object

key

Used with window.find_element and with return values to uniquely identify this element

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

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

str

tooltip

text that will appear when mouse hovers over this element

bool

readonly

make element readonly (user can't change). True means user cannot change

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

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

Returns the current (right now) value of the Combo. DO NOT USE THIS AS THE NORMAL WAY OF READING A COMBO! You should be using values from your call to window.read instead. Know what you're doing if you use it.

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

Changes some of the settings for the Combo Element. Must call `Window.Read` or `Window.Finalize` prior. Note that the state can be in 3 states only.... enabled, disabled, readonly even though more combinations are available. The easy way to remember is that if you change the readonly parameter then you are enabling the element.

Changes will not be visible in your window until you call window.read or window.refresh.

If you change visibility, your element may MOVE. If you want it to remain stationary, use the "layout helper" function "pin" to ensure your element is "pinned" to that location in your layout so that it returns there when made visible.

```
update(value = None,
    values = None,
    set_to_index = None,
    disabled = None,
    readonly = None,
    font = None,
    visible = None,
    size = (None, None))
```

Parameter Descriptions:

Type

Name

Meaning

Any

value

change which value is current selected based on new list of previous list of choices

List[Any]

values

change list of choices

int

set_to_index

change selection to a particular choice starting with index = 0

bool

disabled

disable or enable state of the element

bool

readonly

if True make element readonly (user cannot change any choices). Enables the element if either choice are made.

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

visible

control visibility of element

(int, int)

size

width, height. Width = characters-wide, height = NOTE it's the number of entries to show in the list

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

Returns the current (right now) value of the Combo. DO NOT USE THIS AS THE NORMAL WAY OF READING A COMBO! You should be using values from your call to window.read instead. Know what you're doing if you use it.

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

### Update

Changes some of the settings for the Combo Element. Must call `Window.Read` or `Window.Finalize` prior. Note that the state can be in 3 states only.... enabled, disabled, readonly even though more combinations are available. The easy way to remember is that if you change the readonly parameter then you are enabling the element.

Changes will not be visible in your window until you call window.read or window.refresh.

If you change visibility, your element may MOVE. If you want it to remain stationary, use the "layout helper" function "pin" to ensure your element is "pinned" to that location in your layout so that it returns there when made visible.

```
Update(value = None,
    values = None,
    set_to_index = None,
    disabled = None,
    readonly = None,
    font = None,
    visible = None,
    size = (None, None))
```

Parameter Descriptions:

Type

Name

Meaning

Any

value

change which value is current selected based on new list of previous list of choices

List[Any]

values

change list of choices

int

set_to_index

change selection to a particular choice starting with index = 0

bool

disabled

disable or enable state of the element

bool

readonly

if True make element readonly (user cannot change any choices). Enables the element if either choice are made.

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

visible

control visibility of element

(int, int)

size

width, height. Width = characters-wide, height = NOTE it's the number of entries to show in the list

[Back](./_Elements)
