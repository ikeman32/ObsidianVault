# Debug Window
Works like a "print" statement but with windowing options. Routes output to the "Debug Window"

In addition to the normal text and background colors, you can use a "colors" tuple/string The "colors" or "c" parameter defines both the text and background in a single parm. It can be a tuple or a single single. Both text and background colors need to be specified colors -(str, str) or str. A combined text/background color definition in a single parameter c - (str, str) - Colors tuple has format (foreground, backgrouned) c - str - can also be a string of the format "foreground on background" ("white on red")

```
easy_print(args=*<1 or N object>,
    size = (None, None),
    end = None,
    sep = None,
    location = (None, None),
    relative_location = (None, None),
    font = None,
    no_titlebar = False,
    no_button = False,
    grab_anywhere = False,
    keep_on_top = None,
    do_not_reroute_stdout = True,
    echo_stdout = False,
    text_color = None,
    background_color = None,
    colors = None,
    c = None,
    erase_all = False,
    resizable = True,
    blocking = None,
    wait = None)
```

Parameter Descriptions:

Type

Name

Meaning

Any

*args

stuff to output

(int, int)

size

(w,h) w=characters-wide, h=rows-high

str

end

end character

str

sep

separator character

(int, int)

location

Location of upper left corner of the window

(int, int)

relative_location

(x,y) location relative to the default location of the window, in pixels. Normally the window centers. This location is relative to the location the window would be created. Note they can be negative.

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

no_titlebar

If True no titlebar will be shown

bool

no_button

don't show button

bool

grab_anywhere

If True: can grab anywhere to move the window (Default = False)

str

background_color

color of background

str

text_color

color of the text

bool

keep_on_top

If True the window will remain above all current windows

(int, int)

location

Location of upper left corner of the window

bool

do_not_reroute_stdout

do not reroute stdout and stderr. If False, both stdout and stderr will reroute to here

bool

echo_stdout

If True stdout is sent to both the console and the debug window

str or str, str

colors

Either a tuple or a string that has both the text and background colors

str or str, str

c

Either a tuple or a string that has both the text and background colors

bool

resizable

if True, the user can resize the debug window. Default is True

bool

erase_all

If True when erase the output before printing

(bool or None)

blocking

if True, makes the window block instead of returning immediately. The "Quit" button changers to "More"

(bool or None)

wait

Same as the "blocking" parm. It's an alias. if True, makes the window block instead of returning immediately. The "Quit" button changes to "Click to Continue..."

Close a previously opened EasyPrint window

```
easy_print_close()
```

Works like a "print" statement but with windowing options. Routes output to the "Debug Window"

In addition to the normal text and background colors, you can use a "colors" tuple/string The "colors" or "c" parameter defines both the text and background in a single parm. It can be a tuple or a single single. Both text and background colors need to be specified colors -(str, str) or str. A combined text/background color definition in a single parameter c - (str, str) - Colors tuple has format (foreground, backgrouned) c - str - can also be a string of the format "foreground on background" ("white on red")

```
eprint(args=*<1 or N object>,
    size = (None, None),
    end = None,
    sep = None,
    location = (None, None),
    relative_location = (None, None),
    font = None,
    no_titlebar = False,
    no_button = False,
    grab_anywhere = False,
    keep_on_top = None,
    do_not_reroute_stdout = True,
    echo_stdout = False,
    text_color = None,
    background_color = None,
    colors = None,
    c = None,
    erase_all = False,
    resizable = True,
    blocking = None,
    wait = None)
```

Parameter Descriptions:

Type

Name

Meaning

Any

*args

stuff to output

(int, int)

size

(w,h) w=characters-wide, h=rows-high

str

end

end character

str

sep

separator character

(int, int)

location

Location of upper left corner of the window

(int, int)

relative_location

(x,y) location relative to the default location of the window, in pixels. Normally the window centers. This location is relative to the location the window would be created. Note they can be negative.

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

no_titlebar

If True no titlebar will be shown

bool

no_button

don't show button

bool

grab_anywhere

If True: can grab anywhere to move the window (Default = False)

str

background_color

color of background

str

text_color

color of the text

bool

keep_on_top

If True the window will remain above all current windows

(int, int)

location

Location of upper left corner of the window

bool

do_not_reroute_stdout

do not reroute stdout and stderr. If False, both stdout and stderr will reroute to here

bool

echo_stdout

If True stdout is sent to both the console and the debug window

str or str, str

colors

Either a tuple or a string that has both the text and background colors

str or str, str

c

Either a tuple or a string that has both the text and background colors

bool

resizable

if True, the user can resize the debug window. Default is True

bool

erase_all

If True when erase the output before printing

(bool or None)

blocking

if True, makes the window block instead of returning immediately. The "Quit" button changers to "More"

(bool or None)

wait

Same as the "blocking" parm. It's an alias. if True, makes the window block instead of returning immediately. The "Quit" button changes to "Click to Continue..."

Works like a "print" statement but with windowing options. Routes output to the "Debug Window"

In addition to the normal text and background colors, you can use a "colors" tuple/string The "colors" or "c" parameter defines both the text and background in a single parm. It can be a tuple or a single single. Both text and background colors need to be specified colors -(str, str) or str. A combined text/background color definition in a single parameter c - (str, str) - Colors tuple has format (foreground, backgrouned) c - str - can also be a string of the format "foreground on background" ("white on red")

```
sgprint(args=*<1 or N object>,
    size = (None, None),
    end = None,
    sep = None,
    location = (None, None),
    relative_location = (None, None),
    font = None,
    no_titlebar = False,
    no_button = False,
    grab_anywhere = False,
    keep_on_top = None,
    do_not_reroute_stdout = True,
    echo_stdout = False,
    text_color = None,
    background_color = None,
    colors = None,
    c = None,
    erase_all = False,
    resizable = True,
    blocking = None,
    wait = None)
```

Parameter Descriptions:

Type

Name

Meaning

Any

*args

stuff to output

(int, int)

size

(w,h) w=characters-wide, h=rows-high

str

end

end character

str

sep

separator character

(int, int)

location

Location of upper left corner of the window

(int, int)

relative_location

(x,y) location relative to the default location of the window, in pixels. Normally the window centers. This location is relative to the location the window would be created. Note they can be negative.

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

no_titlebar

If True no titlebar will be shown

bool

no_button

don't show button

bool

grab_anywhere

If True: can grab anywhere to move the window (Default = False)

str

background_color

color of background

str

text_color

color of the text

bool

keep_on_top

If True the window will remain above all current windows

(int, int)

location

Location of upper left corner of the window

bool

do_not_reroute_stdout

do not reroute stdout and stderr. If False, both stdout and stderr will reroute to here

bool

echo_stdout

If True stdout is sent to both the console and the debug window

str or str, str

colors

Either a tuple or a string that has both the text and background colors

str or str, str

c

Either a tuple or a string that has both the text and background colors

bool

resizable

if True, the user can resize the debug window. Default is True

bool

erase_all

If True when erase the output before printing

(bool or None)

blocking

if True, makes the window block instead of returning immediately. The "Quit" button changers to "More"

(bool or None)

wait

Same as the "blocking" parm. It's an alias. if True, makes the window block instead of returning immediately. The "Quit" button changes to "Click to Continue..."

Close a previously opened EasyPrint window

```
sgprint_close()
```

Works like a "print" statement but with windowing options. Routes output to the "Debug Window"

In addition to the normal text and background colors, you can use a "colors" tuple/string The "colors" or "c" parameter defines both the text and background in a single parm. It can be a tuple or a single single. Both text and background colors need to be specified colors -(str, str) or str. A combined text/background color definition in a single parameter c - (str, str) - Colors tuple has format (foreground, backgrouned) c - str - can also be a string of the format "foreground on background" ("white on red")

```
EasyPrint(args=*<1 or N object>,
    size = (None, None),
    end = None,
    sep = None,
    location = (None, None),
    relative_location = (None, None),
    font = None,
    no_titlebar = False,
    no_button = False,
    grab_anywhere = False,
    keep_on_top = None,
    do_not_reroute_stdout = True,
    echo_stdout = False,
    text_color = None,
    background_color = None,
    colors = None,
    c = None,
    erase_all = False,
    resizable = True,
    blocking = None,
    wait = None)
```

Parameter Descriptions:

Type

Name

Meaning

Any

*args

stuff to output

(int, int)

size

(w,h) w=characters-wide, h=rows-high

str

end

end character

str

sep

separator character

(int, int)

location

Location of upper left corner of the window

(int, int)

relative_location

(x,y) location relative to the default location of the window, in pixels. Normally the window centers. This location is relative to the location the window would be created. Note they can be negative.

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

no_titlebar

If True no titlebar will be shown

bool

no_button

don't show button

bool

grab_anywhere

If True: can grab anywhere to move the window (Default = False)

str

background_color

color of background

str

text_color

color of the text

bool

keep_on_top

If True the window will remain above all current windows

(int, int)

location

Location of upper left corner of the window

bool

do_not_reroute_stdout

do not reroute stdout and stderr. If False, both stdout and stderr will reroute to here

bool

echo_stdout

If True stdout is sent to both the console and the debug window

str or str, str

colors

Either a tuple or a string that has both the text and background colors

str or str, str

c

Either a tuple or a string that has both the text and background colors

bool

resizable

if True, the user can resize the debug window. Default is True

bool

erase_all

If True when erase the output before printing

(bool or None)

blocking

if True, makes the window block instead of returning immediately. The "Quit" button changers to "More"

(bool or None)

wait

Same as the "blocking" parm. It's an alias. if True, makes the window block instead of returning immediately. The "Quit" button changes to "Click to Continue..."

Close a previously opened EasyPrint window

```
EasyPrintClose()
```

Works like a "print" statement but with windowing options. Routes output to the "Debug Window"

In addition to the normal text and background colors, you can use a "colors" tuple/string The "colors" or "c" parameter defines both the text and background in a single parm. It can be a tuple or a single single. Both text and background colors need to be specified colors -(str, str) or str. A combined text/background color definition in a single parameter c - (str, str) - Colors tuple has format (foreground, backgrouned) c - str - can also be a string of the format "foreground on background" ("white on red")

```
Print(args=*<1 or N object>,
    size = (None, None),
    end = None,
    sep = None,
    location = (None, None),
    relative_location = (None, None),
    font = None,
    no_titlebar = False,
    no_button = False,
    grab_anywhere = False,
    keep_on_top = None,
    do_not_reroute_stdout = True,
    echo_stdout = False,
    text_color = None,
    background_color = None,
    colors = None,
    c = None,
    erase_all = False,
    resizable = True,
    blocking = None,
    wait = None)
```

Parameter Descriptions:

Type

Name

Meaning

Any

*args

stuff to output

(int, int)

size

(w,h) w=characters-wide, h=rows-high

str

end

end character

str

sep

separator character

(int, int)

location

Location of upper left corner of the window

(int, int)

relative_location

(x,y) location relative to the default location of the window, in pixels. Normally the window centers. This location is relative to the location the window would be created. Note they can be negative.

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

bool

no_titlebar

If True no titlebar will be shown

bool

no_button

don't show button

bool

grab_anywhere

If True: can grab anywhere to move the window (Default = False)

str

background_color

color of background

str

text_color

color of the text

bool

keep_on_top

If True the window will remain above all current windows

(int, int)

location

Location of upper left corner of the window

bool

do_not_reroute_stdout

do not reroute stdout and stderr. If False, both stdout and stderr will reroute to here

bool

echo_stdout

If True stdout is sent to both the console and the debug window

str or str, str

colors

Either a tuple or a string that has both the text and background colors

str or str, str

c

Either a tuple or a string that has both the text and background colors

bool

resizable

if True, the user can resize the debug window. Default is True

bool

erase_all

If True when erase the output before printing

(bool or None)

blocking

if True, makes the window block instead of returning immediately. The "Quit" button changers to "More"

(bool or None)

wait

Same as the "blocking" parm. It's an alias. if True, makes the window block instead of returning immediately. The "Quit" button changes to "Click to Continue..."

Close a previously opened EasyPrint window

```
PrintClose()
```

[Back](./_Elements)
