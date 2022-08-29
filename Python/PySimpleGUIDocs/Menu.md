# Menu
```
Menu Element is the Element that provides a Menu Bar that goes across the top of the window, just below titlebar.
Here is an example layout.  The "&" are shortcut keys ALT+key.
Is a List of -  "Item String" + List
Where Item String is what will be displayed on the Menubar itself.
The List that follows the item represents the items that are shown then Menu item is clicked
Notice how an "entry" in a mennu can be a list which means it branches out and shows another menu, etc. (resursive)
menu_def = [['&File', ['!&Open', '&Save::savekey', '---', '&Properties', 'E&xit']],
            ['!&Edit', ['!&Paste', ['Special', 'Normal', ], 'Undo'], ],
            ['&Debugger', ['Popout', 'Launch Debugger']],
            ['&Toolbar', ['Command &1', 'Command &2', 'Command &3', 'Command &4']],
            ['&Help', '&About...'], ]
Important Note!  The colors, font, look of the Menubar itself cannot be changed, only the menus shown AFTER clicking the menubar
can be changed.  If you want to change the style/colors the Menubar, then you will have to use the MenubarCustom element.
Finally, "keys" can be added to entries so make them unique.  The "Save" entry has a key associated with it. You
can see it has a "::" which signifies the beginning of a key.  The user will not see the key portion when the
menu is shown.  The key portion is returned as part of the event.
```

```
Menu(menu_definition,
    background_color = None,
    text_color = None,
    disabled_text_color = None,
    size = (None, None),
    s = (None, None),
    tearoff = False,
    font = None,
    pad = None,
    p = None,
    key = None,
    k = None,
    visible = True,
    metadata = None)
```

Parameter Descriptions:

Type

Name

Meaning

List[List[Tuple[str, List[str]]]

menu_definition

The Menu definition specified using lists (docs explain the format)

str

background_color

color of the background of menus, NOT the Menubar

str

text_color

text color for menus, NOT the Menubar. Can be in #RRGGBB format or a color name "black".

str

disabled_text_color

color to use for text when item in submenu, not the menubar itself, is disabled. Can be in #RRGGBB format or a color name "black"

(int, int)

size

Not used in the tkinter port

(int, int) or (None, None)

s

Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used

bool

tearoff

if True, then can tear the menu off from the window ans use as a floating window. Very cool effect

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. of submenus. Does NOT apply to the Menubar itself. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

str or int or tuple or object

key

Value that uniquely identifies this element from all other elements. Used when Finding an element or in return values. Must be unique to the window

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

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

Update a menubar - can change the menu definition and visibility. The entire menu has to be specified

Changes will not be visible in your window until you call window.read or window.refresh.

If you change visibility, your element may MOVE. If you want it to remain stationary, use the "layout helper" function "pin" to ensure your element is "pinned" to that location in your layout so that it returns there when made visible.

```
update(menu_definition = None, visible = None)
```

Parameter Descriptions:

Type

Name

Meaning

List[List[Tuple[str, List[str]]]

menu_definition

The menu definition list

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

Update a menubar - can change the menu definition and visibility. The entire menu has to be specified

Changes will not be visible in your window until you call window.read or window.refresh.

If you change visibility, your element may MOVE. If you want it to remain stationary, use the "layout helper" function "pin" to ensure your element is "pinned" to that location in your layout so that it returns there when made visible.

```
Update(menu_definition = None, visible = None)
```

Parameter Descriptions:

Type

Name

Meaning

List[List[Tuple[str, List[str]]]

menu_definition

The menu definition list

bool

visible

control visibility of element

[Back](./_Elements)
