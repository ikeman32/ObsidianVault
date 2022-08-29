# Menubar Custom
Note that while the MenubarCustom is an element, it is implemented using a function. It is actually a "compound element" that consists of several elements combined into a single Column element. See the Column element to get a list of method calls available. The function returns a Column element.

A custom Menubar that replaces the OS provided Menubar

Why? Two reasons - 1. they look great (see custom titlebar) 2. if you have a custom titlebar, then you have to use a custom menubar if you want a menubar

```
MenubarCustom(menu_definition,
    disabled_text_color = None,
    bar_font = None,
    font = None,
    tearoff = False,
    pad = 0,
    p = None,
    background_color = None,
    text_color = None,
    bar_background_color = None,
    bar_text_color = None,
    key = None,
    k = None)
```

Parameter Descriptions:

Type

Name

Meaning

List[List[Tuple[str, List[str]]]

menu_definition

The Menu definition specified using lists (docs explain the format)

str

disabled_text_color

color to use for text when item is disabled. Can be in #RRGGBB format or a color name "black"

(str or (str, int[, str]) or None)

bar_font

specifies the font family, size to be used for the chars in the bar itself

(str or (str, int[, str]) or None)

font

specifies the font family, size to be used for the menu items

bool

tearoff

if True, then can tear the menu off from the window ans use as a floating window. Very cool effect

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int). TIP - 0 will make flush with titlebar

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

str

background_color

color to use for background of the menus that are displayed after making a section. Can be in #RRGGBB format or a color name "black". Defaults to the color of the bar text

str

text_color

color to use for the text of the many items in the displayed menus. Can be in #RRGGBB format or a color name "black". Defaults to the bar background

str

bar_background_color

color to use for the menubar. Can be in #RRGGBB format or a color name "black". Defaults to theme's button text color

str

bar_text_color

color to use for the menu items text when item is disabled. Can be in #RRGGBB format or a color name "black". Defaults to theme's button background color

str or int or tuple or object

key

Value that uniquely identifies this element from all other elements. Used when Finding an element or in return values. Must be unique to the window

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

[Back](./_Elements)