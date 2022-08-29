# Color Printing - Multiline
Color print to a multiline element in a window of your choice. Must have EITHER called cprint_set_output_destination prior to making this call so that the window and element key can be saved and used here to route the output, OR used the window and key parameters to the cprint function to specicy these items.

args is a variable number of things you want to print.

end - The end char to use just like print uses sep - The separation character like print uses text_color - The color of the text key - overrides the previously defined Multiline key window - overrides the previously defined window to output to background_color - The color of the background colors -(str, str) or str. A combined text/background color definition in a single parameter

There are also "aliases" for text_color, background_color and colors (t, b, c) t - An alias for color of the text (makes for shorter calls) b - An alias for the background_color parameter c - (str, str) - "shorthand" way of specifying color. (foreground, backgrouned) c - str - can also be a string of the format "foreground on background" ("white on red")

With the aliases it's possible to write the same print but in more compact ways: cprint('This will print white text on red background', c=('white', 'red')) cprint('This will print white text on red background', c='white on red') cprint('This will print white text on red background', text_color='white', background_color='red') cprint('This will print white text on red background', t='white', b='red')

```
cprint(args=*<1 or N object>,
    end = None,
    sep = " ",
    text_color = None,
    font = None,
    t = None,
    background_color = None,
    b = None,
    colors = None,
    c = None,
    window = None,
    key = None,
    justification = None,
    autoscroll = True,
    erase_all = False)
```

Parameter Descriptions:

Type

Name

Meaning

Any

*args

stuff to output

str

text_color

Color of the text

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike for the value being updated

str

background_color

The background color of the line

str or str, str

colors

Either a tuple or a string that has both the text and background colors "text on background" or just the text color

str

t

Color of the text

str

b

The background color of the line

str or str, str

c

Either a tuple or a string. Same as the color parm

str

end

end character

str

sep

separator character

Any

key

key of multiline to output to (if you want to override the one previously set)

Window

window

Window containing the multiline to output to (if you want to override the one previously set)

str

justification

text justification. left, right, center. Can use single characters l, r, c. Sets only for this value, not entire element

bool

autoscroll

If True the contents of the element will automatically scroll as more data added to the end

Sets up the color print (cprint) output destination

```
cprint_set_output_destination(window, multiline_key)
```

Parameter Descriptions:

Type

Name

Meaning

Window

window

The window that the cprint call will route the output to

Any

multiline_key

Key for the Multiline Element where output will be sent

None

**RETURN**

None

[Back](./_Elements)
