# Button Element
```
Button Element - Defines all possible buttons. The shortcuts such as Submit, FileBrowse, ... each create a Button
```

```
Button(button_text = "",
    button_type = 7,
    target = (None, None),
    tooltip = None,
    file_types = (('ALL Files', '*.* *'),),
    initial_folder = None,
    default_extension = "",
    disabled = False,
    change_submits = False,
    enable_events = False,
    image_filename = None,
    image_data = None,
    image_size = (None, None),
    image_subsample = None,
    image_source = None,
    border_width = None,
    size = (None, None),
    s = (None, None),
    auto_size_button = None,
    button_color = None,
    disabled_button_color = None,
    highlight_colors = None,
    mouseover_colors = (None, None),
    use_ttk_buttons = None,
    font = None,
    bind_return_key = False,
    focus = False,
    pad = None,
    p = None,
    key = None,
    k = None,
    right_click_menu = None,
    expand_x = False,
    expand_y = False,
    visible = True,
    metadata = None)
```

**Parameter Descriptions**:

| **Type**                 | **Name**          | **Meaning**                                                                                                                                                                                                                     |
| ------------------------ | ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| str                      | button_text       | Text to be displayed on the button                                                                                                                                                                                              |
| int                      | button_type       | You should NOT be setting this directly. ONLY the shortcut functions set this                                                                                                                                                   |
| str or (int, int)        | target            | key or (row,col) target for the button. Note that -1 for column means 1 element to the left of this one. The constant ThisRow is used to indicate the current row. The Button itself is a valid target for some types of button |
| str                      | tooltip           | text, that will appear when mouse hovers over the element                                                                                                                                                                       |
| Tuple\[(str, str), ...\] | file_types        | the filetypes that will be used to match files. To indicate all files: (("ALL Files", "_._ \*"),\)\.                                                                                                                            |
| str                      | initial_folder    | starting path for folders and files                                                                                                                                                                                             |
| str                      | default_extension | If no extension entered by user, add this to filename (only used in saveas dialogs)                                                                                                                                             |
| (bool or str)            | disabled          | If True button will be created disabled. If BUTTON_DISABLED_MEANS_IGNORE then the button will be ignored rather than disabled using tkinter                                                                                     |
|bool                          |change_submits                   |DO NOT USE. Only listed for backwards compat - Use enable_events instead                                                                                                                                                                                                                                 |
|bool|enable_events|Turns on the element specific events. If this button is a target, should it generate an event when filled in|
|(str or bytes)|image_source|Image to place on button. Use INSTEAD of the image_filename and image_data. Unifies these into 1 easier to use parm|
|str|image_filename|image filename if there is a button image. GIFs and PNGs only.|
|bytes or str|image_data|Raw or Base64 representation of the image to put on button. Choose either filename or data|
|(int, int)|image_size|Size of the image in pixels (width, height)|
|int|image_subsample|amount to reduce the size of the image. Divides the size by this number. 2=1/2, 3=1/3, 4=1/4, etc|
|int|border_width|width of border around button in pixels|
|(int or None, int or None) or (None, None) or int|size|(w, h) w=characters-wide, h=rows-high. If an int instead of a tuple is supplied, then height is auto-set to 1|
|(int or None, int or None) or (None, None) or int|s|Same as size parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, size will be used|
|bool|auto_size_button|if True the button size is sized to fit the text|
|(str, str) or str or (int, int) or None|button_color|Color of button. default is from theme or the window. Easy to remember which is which if you say "ON" between colors. "red" on "green". Normally a tuple, but can be a simplified-button-color-string "foreground on background". Can be a single color if want to set only the background.|
|(str, str) or str|disabled_button_color|colors to use when button is disabled (text, background). Use None for a color if don't want to change. Only ttk buttons support both text and background colors. tk buttons only support changing text color|
|(str, str)|highlight_colors|colors to use when button has focus (has focus, does not have focus). None will use colors based on theme. Only used by Linux and only for non-TTK button|
|(str, str) or str|mouseover_colors|Important difference between Linux & Windows! Linux - Colors when mouse moved over button. Windows - colors when button is pressed. The default is to switch the text and background colors (an inverse effect)|
|bool|use_ttk_buttons|True = use ttk buttons. False = do not use ttk buttons. None (Default) = use ttk buttons only if on a Mac and not with button images|
|\(str or \(str, int\[, str\]\) or None\)|font|specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike|
|bool|bind_return_key|If True the return key will cause this button to be pressed|
|bool|focus|if True, initial focus will be put on this button|
|(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int|pad|Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)|
|(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int|p|Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used|
|str or int or tuple or object|key|Used with window.find_element and with return values to uniquely identify this element to uniquely identify this element|
|str or int or tuple or object|k|Same as the Key. You can use either k or key. Which ever is set will be used.|
|List\[List\[ List\[str\] or str \]\]|right_click_menu|A list of lists of Menu items to show when this element is right clicked. See user docs for exact format.|
|bool|expand_x|If True the element will automatically expand in the X direction to fill available space|
|bool|expand_y|If True the element will automatically expand in the Y direction to fill available space|
|bool|visible|set visibility state of the element|
|Any|metadata|User metadata that can be set to ANYTHING|

### bind

Used to add tkinter events to an Element. The tkinter specific data is in the Element's member variable user_bind_event

``` python,
bind(bind_string, 
	key_modifier, 
	propagate = True)
```

**Parameter Descriptions**:

| **Type** | **Name** | **Meaning** |
| -------- | -------- | ----------- |
|str          |bind_string          |The string tkinter expected in its bind function             |
|str|key_modifier|Additional data to be added to the element's key when event is returned|
|bool|propagate|If True then tkinter will be told to propagate the event to the element|

### block_focus

Enable or disable the element from getting focus by using the keyboard. If the block parameter is True, then this element will not be given focus by using the keyboard to go from one element to another. You CAN click on the element and utilize it.

``` python,
block_focus(block = True)
```

Parameter Descriptions:

| Type | Name | Meaning |
| ---- | ---- | ------- |
|bool      |block      |if True the element will not get focus via the keyboard         |

### click

Generates a click of the button as if the user clicked the button Calls the tkinter invoke method for the button

```python,
click()
```

### expand

Causes the Element to expand to fill available space in the X and Y directions. Can specify which or both directions

``` python,
expand(expand_x = False,
    expand_y = False,
    expand_row = True)
```

Parameter Descriptions:

| Type | Name | Meaning |
| ---- | ---- | ------- |
|bool      |expand_x      |If True Element will expand in the Horizontal directions         |
|bool|expand_y|If True Element will expand in the Vertical directions|
|bool|expand_row|If True the row containing the element will also expand. Without this your element is "trapped" within the row|

### get_next_focus

Gets the next element that should get focus after this element.
`
``` python,
get_next_focus()
```

| Type | Name | Meaning |
| ---- | ---- | ------- |
|(Element)     |**return**      |Element that will get focus after this one         |

### get_previous_focus

Gets the element that should get focus previous to this element.
``` python,
get_previous_focus()
```

| Type | Name | Meaning |
| ---- | ---- | ------- |
|(Element)      |**return**      |Element that should get the focus before this one         |

### get_size

Return the size of an element in Pixels. Care must be taken as some elements use characters to specify their size but will return pixels when calling this get_size method.
``` python,
get_size()
```

| Type | Name | Meaning |
| ---- | ---- | ------- |
|(int, int)      |**return**      |width and height of the element         |

### get_text

Returns the current text shown on a button

``` python,
get_text()
```


| Type  | Name       | Meaning                                    |
| ----- | ---------- | ------------------------------------------ |
| (str) | **return** | The text currently displayed on the button |

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

| Type  | Name       | Meaning          |
| ----- | ---------- | ---------------- |
| (Any) | **return** | The window's Key |

### metadata

#### property: metadata

Metadata is an Element property that you can use at any time to hold any value

| Type  | Name       | Meaning                    |
| ----- | ---------- | -------------------------- |
| (Any) | **return** | the current metadata value |

### set_cursor

Sets the cursor for the current Element. "Cursor" is used in 2 different ways in this call. For the parameter "cursor" it's actually the mouse pointer. If you do not want any mouse pointer, then use the string "none" For the parameter "cursor_color" it's the color of the beam used when typing into an input element

```python
set_cursor(cursor = None, cursor_color = None)
```

Parameter Descriptions:

| Type | Name         | Meaning                      |
| ---- | ------------ | ---------------------------- |
| str  | cursor       | The tkinter cursor name      |
| str  | cursor_color | color to set the "cursor" to |

### set_focus

Sets the current focus to be on this element

```python
set_focus(force = False)
```

Parameter Descriptions:

| Type | Name  | Meaning                                                 |
| ---- | ----- | ------------------------------------------------------- |
| bool | force | if True will call focus_force otherwise calls focus_set |

### set_size

Changes the size of an element to a specific size. It's possible to specify None for one of sizes so that only 1 of the element's dimensions are changed.

```python
set_size(size = (None, None))
```

Parameter Descriptions:

| Type       | Name | Meaning                                                               |
| ---------- | ---- | --------------------------------------------------------------------- |
| (int, int) | size | The size in characters, rows typically. In some cases they are pixels |

### set_tooltip

Called by application to change the tooltip text for an Element. Normally invoked using the Element Object such as: window.Element('key').SetToolTip('New tip').

```python
set_tooltip(tooltip_text)
```

Parameter Descriptions:

| Type | Name         | Meaning                      |
| ---- | ------------ | ---------------------------- |
| str  | tooltip_text | the text to show in tooltip. |

### set_vscroll_position

Attempts to set the vertical scroll postition for an element's Widget

```python
set_vscroll_position(percent_from_top)
```

Parameter Descriptions:

| Type  | Name             | Meaning                                                         |
| ----- | ---------------- | --------------------------------------------------------------- |
| float | percent_from_top | From 0 to 1.0, the percentage from the top to move scrollbar to |

### unbind

Removes a previously bound tkinter event from an Element.

```python
unbind(bind_string)
```

Parameter Descriptions:

| Type | Name        | Meaning                                          |
| ---- | ----------- | ------------------------------------------------ |
| str  | bind_string | The string tkinter expected in its bind function |

### unhide_row

Unhides (makes visible again) the row container that the Element is located on. Note that it will re-appear at the bottom of the window / container, most likely.

```python
unhide_row()
```

### update

Changes some of the settings for the Button Element. Must call `Window.Read` or `Window.Finalize` prior

Changes will not be visible in your window until you call window.read or window.refresh.

If you change visibility, your element may MOVE. If you want it to remain stationary, use the "layout helper" function "pin" to ensure your element is "pinned" to that location in your layout so that it returns there when made visible.

```python
update(text = None,
    button_color = (None, None),
    disabled = None,
    image_data = None,
    image_filename = None,
    visible = None,
    image_subsample = None,
    disabled_button_color = (None, None),
    image_size = None)
```

Parameter Descriptions:

| Type                                    | Name                  | Meaning                                                                                                                                                                                                                                                                                     |
| --------------------------------------- | --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| str                                     | text                  | sets button text                                                                                                                                                                                                                                                                            |
| (str, str) or str or (int, int) or None | button_color          | Color of button. default is from theme or the window. Easy to remember which is which if you say "ON" between colors. "red" on "green". Normally a tuple, but can be a simplified-button-color-string "foreground on background". Can be a single color if want to set only the background. |
| (bool or str)                           | disabled              | True/False to enable/disable at the GUI level. Use BUTTON_DISABLED_MEANS_IGNORE to ignore clicks (won't change colors)                                                                                                                                                                      |
| bytes or str                            | image_data            | Raw or Base64 representation of the image to put on button. Choose either filename or data                                                                                                                                                                                                  |
| str                                     | image_filename        | image filename if there is a button image. GIFs and PNGs only.                                                                                                                                                                                                                              |
| (str, str)                              | disabled_button_color | colors to use when button is disabled (text, background). Use None for a color if don't want to change. Only ttk buttons support both text and background colors. tk buttons only support changing text color                                                                               |
| bool                                    | visible               | control visibility of element                                                                                                                                                                                                                                                               |
| int                                     | image_subsample       | amount to reduce the size of the image. Divides the size by this number. 2=1/2, 3=1/3, 4=1/4, etc                                                                                                                                                                                           |
| (int, int)                              | image_size            | Size of the image in pixels (width, height)                                                                                                                                                                                                                                                 |

### visible

#### property: visible

Returns visibility state for the element. This is a READONLY property

| Type   | Name       | Meaning                      |
| ------ | ---------- | ---------------------------- |
| (bool) | **return** | Visibility state for element |

### widget

#### property: widget

Returns tkinter widget for the element. This is a READONLY property. The implementation is that the Widget member variable is returned. This is a backward compatible addition

| Type             | Name       | Meaning                                 |
| ---------------- | ---------- | --------------------------------------- |
| (tkinter.Widget) | **return** | The element's underlying tkinter widget |

---

### These are non-PEP8 Compliant Methods - do NOT use

The following methods are here for backwards compatibility reference. You will find there are PEP8 versions for each of these methods. The PEP8 versions will be all lower case and have underscores.

### Click

Generates a click of the button as if the user clicked the button Calls the tkinter invoke method for the button

```python
Click()
```

### GetText

Returns the current text shown on a button

```python
GetText()
```

| Type  | Name       | Meaning                                    |
| ----- | ---------- | ------------------------------------------ |
| (str) | **return** | The text currently displayed on the button |

### SetFocus

Sets the current focus to be on this element

``` python
SetFocus(force = False)
```

Parameter Descriptions:

| Type | Name | Meaning |
| ---- | ---- | ------- |
|      |      |         |
bool|force|if True will call focus_force otherwise calls focus_set|

### SetTooltip

Called by application to change the tooltip text for an Element. Normally invoked using the Element Object such as: window.Element('key').SetToolTip('New tip').

```python
SetTooltip(tooltip_text)
```

Parameter Descriptions:

| Type | Name         | Meaning                      |
| ---- | ------------ | ---------------------------- |
| str  | tooltip_text | the text to show in tooltip. |

### Update

Changes some of the settings for the Button Element. Must call `Window.Read` or `Window.Finalize` prior

Changes will not be visible in your window until you call window.read or window.refresh.

If you change visibility, your element may MOVE. If you want it to remain stationary, use the "layout helper" function "pin" to ensure your element is "pinned" to that location in your layout so that it returns there when made visible.

```
Update(text = None,
    button_color = (None, None),
    disabled = None,
    image_data = None,
    image_filename = None,
    visible = None,
    image_subsample = None,
    disabled_button_color = (None, None),
    image_size = None)
```

Parameter Descriptions:

| Type                                    | Name                  | Meaning                                                                                                                                                                                                                                                                                     |
| --------------------------------------- | --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| str                                     | text                  | sets button text                                                                                                                                                                                                                                                                            |
| (str, str) or str or (int, int) or None | button_color          | Color of button. default is from theme or the window. Easy to remember which is which if you say "ON" between colors. "red" on "green". Normally a tuple, but can be a simplified-button-color-string "foreground on background". Can be a single color if want to set only the background. |
| (bool or str)                           | disabled              | True/False to enable/disable at the GUI level. Use BUTTON_DISABLED_MEANS_IGNORE to ignore clicks (won't change colors)                                                                                                                                                                      |
| bytes or str                            | image_data            | Raw or Base64 representation of the image to put on button. Choose either filename or data                                                                                                                                                                                                  |
| str                                     | image_filename        | image filename if there is a button image. GIFs and PNGs only.                                                                                                                                                                                                                              |
| (str, str)                              | disabled_button_color | colors to use when button is disabled (text, background). Use None for a color if don't want to change. Only ttk buttons support both text and background colors. tk buttons only support changing text color                                                                               |
| bool                                    | visible               | control visibility of element                                                                                                                                                                                                                                                               |
| int                                     | image_subsample       | amount to reduce the size of the image. Divides the size by this number. 2=1/2, 3=1/3, 4=1/4, etc                                                                                                                                                                                           |
| (int, int)                              | image_size            | Size of the image in pixels (width, height)                                                                                                                                                                                                                                                 |

[Back](./_Elements)
