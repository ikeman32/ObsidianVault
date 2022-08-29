# One Line Progress Meter
Add a progress meter to your application by adding 1 line of code.

```
one_line_progress_meter(title,
    current_value,
    max_value,
    args=*<1 or N object>,
    key = "OK for 1 meter",
    orientation = "v",
    bar_color = (None, None),
    button_color = None,
    size = (20, 20),
    border_width = None,
    grab_anywhere = False,
    no_titlebar = False,
    keep_on_top = None,
    no_button = False)
```

Parameter Descriptions:

Type

Name

Meaning

str

title

text to display in eleemnt

int

current_value

current value

int

max_value

max value of QuickMeter

Any

*args

stuff to output

str or int or tuple or object

key

Used to differentiate between mutliple meters. Used to cancel meter early. Now optional as there is a default value for single meters

str

orientation

'horizontal' or 'vertical' ('h' or 'v' work) (Default value = 'vertical' / 'v')

Tuple(str, str)

bar_color

color of a bar line

(str, str) or str

button_color

button color (foreground, background)

(int, int)

size

(w,h) w=characters-wide, h=rows-high (Default value = DEFAULT_PROGRESS_BAR_SIZE)

int

border_width

width of border around element

bool

grab_anywhere

If True: can grab anywhere to move the window (Default = False)

bool

no_titlebar

If True: no titlebar will be shown on the window

bool

keep_on_top

If True the window will remain above all current windows

bool

no_button

If True: window will be created without a cancel button

(bool)

**RETURN**

True if updated successfully. False if user closed the meter with the X or Cancel button

Cancels and closes a previously created One Line Progress Meter window

```
one_line_progress_meter_cancel(key = "OK for 1 meter")
```

Parameter Descriptions:

Type

Name

Meaning

Any

key

Key used when meter was created

None

**RETURN**

None

### NON-PEP8 Versions

Don't use these. They are here in case you're searching for them. Instead use the PEP8 version `one_line_progress_meter`.

```
OneLineProgressMeter(title,
    current_value,
    max_value,
    args=*<1 or N object>,
    key = "OK for 1 meter",
    orientation = "v",
    bar_color = (None, None),
    button_color = None,
    size = (20, 20),
    border_width = None,
    grab_anywhere = False,
    no_titlebar = False,
    keep_on_top = None,
    no_button = False)
```

Parameter Descriptions:

Type

Name

Meaning

str

title

text to display in eleemnt

int

current_value

current value

int

max_value

max value of QuickMeter

Any

*args

stuff to output

str or int or tuple or object

key

Used to differentiate between mutliple meters. Used to cancel meter early. Now optional as there is a default value for single meters

str

orientation

'horizontal' or 'vertical' ('h' or 'v' work) (Default value = 'vertical' / 'v')

Tuple(str, str)

bar_color

color of a bar line

(str, str) or str

button_color

button color (foreground, background)

(int, int)

size

(w,h) w=characters-wide, h=rows-high (Default value = DEFAULT_PROGRESS_BAR_SIZE)

int

border_width

width of border around element

bool

grab_anywhere

If True: can grab anywhere to move the window (Default = False)

bool

no_titlebar

If True: no titlebar will be shown on the window

bool

keep_on_top

If True the window will remain above all current windows

bool

no_button

If True: window will be created without a cancel button

(bool)

**RETURN**

True if updated successfully. False if user closed the meter with the X or Cancel button

Cancels and closes a previously created One Line Progress Meter window

```
OneLineProgressMeterCancel(key = "OK for 1 meter")
```

Parameter Descriptions:

Type

Name

Meaning

Any

key

Key used when meter was created

None

**RETURN**

None

[Back](./_Elements)
