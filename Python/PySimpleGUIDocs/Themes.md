# Themes
he way to get Windows that have elements that have matching colors.

Sets / Gets the current Theme. If none is specified then returns the current theme. This call replaces the ChangeLookAndFeel / change_look_and_feel call which only sets the theme.

```
theme(new_theme = None)
```

Parameter Descriptions:

Type

Name

Meaning

str

new_theme

the new theme name to use

(str)

**RETURN**

the currently selected theme

Add a new theme to the dictionary of themes

```
theme_add_new(new_theme_name, new_theme_dict)
```

Parameter Descriptions:

Type

Name

Meaning

str

new_theme_name

text to display in element

dict

new_theme_dict

text to display in element

Sets/Returns the background color currently in use Used for Windows and containers (Column, Frame, Tab) and tables

```
theme_background_color(color = None)
```

Parameter Descriptions:

Type

Name

Meaning

str

color

new background color to use (optional)

(str)

**RETURN**

color string of the background color currently in use

Sets/Returns the border width currently in use Used by non ttk elements at the moment

```
theme_border_width(border_width = None)
```

Parameter Descriptions:

Type

Name

Meaning

(int)

**RETURN**

border width currently in use

Sets/Returns the button color currently in use

```
theme_button_color(color = None)
```

Parameter Descriptions:

Type

Name

Meaning

(str, str)

**RETURN**

(str, str) - TUPLE with color strings of the button color currently in use (button text color, button background color)

Returns the button color background currently in use. Note this function simple calls the theme_button_color function and splits apart the tuple

```
theme_button_color_background()
```

Parameter Descriptions:

Type

Name

Meaning

(str)

**RETURN**

color string of the button color background currently in use

Returns the button color text currently in use. Note this function simple calls the theme_button_color function and splits apart the tuple

```
theme_button_color_text()
```

Parameter Descriptions:

Type

Name

Meaning

(str)

**RETURN**

color string of the button color text currently in use

Sets/Returns the background color currently in use for all elements except containers

```
theme_element_background_color(color = None)
```

Parameter Descriptions:

Type

Name

Meaning

(str)

**RETURN**

(str) - color string of the element background color currently in use

Sets/Returns the text color used by elements that have text as part of their display (Tables, Trees and Sliders)

```
theme_element_text_color(color = None)
```

Parameter Descriptions:

Type

Name

Meaning

(str)

**RETURN**

color string currently in use

Sets / Gets the global PySimpleGUI Theme. If none is specified then returns the global theme from user settings. Note the theme must be a standard, built-in PySimpleGUI theme... not a user-created theme.

```
theme_global(new_theme = None)
```

Parameter Descriptions:

Type

Name

Meaning

str

new_theme

the new theme name to use

(str)

**RETURN**

the currently selected theme

Sets/Returns the input element background color currently in use

```
theme_input_background_color(color = None)
```

Parameter Descriptions:

Type

Name

Meaning

(str)

**RETURN**

(str) - color string of the input element background color currently in use

Sets/Returns the input element entry color (not the text but the thing that's displaying the text)

```
theme_input_text_color(color = None)
```

Parameter Descriptions:

Type

Name

Meaning

(str)

**RETURN**

(str) - color string of the input element color currently in use

Returns a sorted list of the currently available color themes

```
theme_list()
```

Parameter Descriptions:

Type

Name

Meaning

List[str]

**RETURN**

A sorted list of the currently available color themes

Displays a "Quick Reference Window" showing all of the different Look and Feel settings that are available. They are sorted alphabetically. The legacy color names are mixed in, but otherwise they are sorted into Dark and Light halves

```
theme_previewer(columns = 12,
    scrollable = False,
    scroll_area_size = (None, None),
    search_string = None,
    location = (None, None))
```

Parameter Descriptions:

Type

Name

Meaning

int

columns

The number of themes to display per row

bool

scrollable

If True then scrollbars will be added

(int, int)

scroll_area_size

Size of the scrollable area (The Column Element used to make scrollable)

str

search_string

If specified then only themes containing this string will be shown

(int, int)

location

Location on the screen to place the window. Defaults to the center like all windows

Display themes in a window as color swatches. Click on a color swatch to see the hex value printed on the console. If you hover over a color or right click it you'll also see the hext value.

```
theme_previewer_swatches()
```

Sets/Returns the progress meter border width currently in use

```
theme_progress_bar_border_width(border_width = None)
```

Parameter Descriptions:

Type

Name

Meaning

(int)

**RETURN**

border width currently in use for progress meters

Sets/Returns the progress bar colors by the current color theme

```
theme_progress_bar_color(color = None)
```

Parameter Descriptions:

Type

Name

Meaning

(str, str)

**RETURN**

(str, str) - TUPLE with color strings of the ProgressBar color currently in use(button text color, button background color)

Sets/Returns the slider border width currently in use

```
theme_slider_border_width(border_width = None)
```

Parameter Descriptions:

Type

Name

Meaning

(int)

**RETURN**

border width currently in use for sliders

Sets/Returns the slider color (used for sliders)

```
theme_slider_color(color = None)
```

Parameter Descriptions:

Type

Name

Meaning

(str)

**RETURN**

color string of the slider color currently in use

Sets/Returns the text color currently in use

```
theme_text_color(color = None)
```

Parameter Descriptions:

Type

Name

Meaning

(str)

**RETURN**

(str) - color string of the text color currently in use

Sets/Returns the background color for text elements

```
theme_text_element_background_color(color = None)
```

Parameter Descriptions:

Type

Name

Meaning

(str)

**RETURN**

(str) - color string of the text background color currently in use

Returns True if a custom titlebar will be / should be used. The setting is in the Global Settings window and can be overwridden using set_options call

```
theme_use_custom_titlebar()
```

Parameter Descriptions:

Type

Name

Meaning

(bool)

**RETURN**

True if a custom titlebar / custom menubar should be used

[Back](./_Elements)
