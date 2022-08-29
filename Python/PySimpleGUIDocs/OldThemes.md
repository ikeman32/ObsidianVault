# Old Themes
You should NOT use these calls. They are here for your reference should you run into them in existing code.

Change the "color scheme" of all future PySimpleGUI Windows. The scheme are string names that specify a group of colors. Background colors, text colors, button colors. There are 13 different color settings that are changed at one time using a single call to ChangeLookAndFeel The look and feel table itself has these indexes into the dictionary LOOK_AND_FEEL_TABLE. The original list was (prior to a major rework and renaming)... these names still work... In Nov 2019 a new Theme Formula was devised to make choosing a theme easier: The "Formula" is: ["Dark" or "Light"] Color Number Colors can be Blue Brown Grey Green Purple Red Teal Yellow Black The number will vary for each pair. There are more DarkGrey entries than there are LightYellow for example. Default = The default settings (only button color is different than system default) Default1 = The full system default including the button (everything's gray... how sad... don't be all gray... please....)

```
ChangeLookAndFeel(index, force = False)
```

Parameter Descriptions:

Type

Name

Meaning

str

index

the name of the index into the Look and Feel table (does not have to be exact, can be "fuzzy")

bool

force

no longer used

None

**RETURN**

None

Get a list of the valid values to pass into your call to change_look_and_feel

```
ListOfLookAndFeelValues()
```

Parameter Descriptions:

Type

Name

Meaning

List[str]

**RETURN**

list of valid string values

Displays a "Quick Reference Window" showing all of the different Look and Feel settings that are available. They are sorted alphabetically. The legacy color names are mixed in, but otherwise they are sorted into Dark and Light halves

```
preview_all_look_and_feel_themes(columns = 12,
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

Get a list of the valid values to pass into your call to change_look_and_feel

```
list_of_look_and_feel_values()
```

Parameter Descriptions:

Type

Name

Meaning

List[str]

**RETURN**

list of valid string values

Change the "color scheme" of all future PySimpleGUI Windows. The scheme are string names that specify a group of colors. Background colors, text colors, button colors. There are 13 different color settings that are changed at one time using a single call to ChangeLookAndFeel The look and feel table itself has these indexes into the dictionary LOOK_AND_FEEL_TABLE. The original list was (prior to a major rework and renaming)... these names still work... In Nov 2019 a new Theme Formula was devised to make choosing a theme easier: The "Formula" is: ["Dark" or "Light"] Color Number Colors can be Blue Brown Grey Green Purple Red Teal Yellow Black The number will vary for each pair. There are more DarkGrey entries than there are LightYellow for example. Default = The default settings (only button color is different than system default) Default1 = The full system default including the button (everything's gray... how sad... don't be all gray... please....)

```
change_look_and_feel(index, force = False)
```

Parameter Descriptions:

Type

Name

Meaning

str

index

the name of the index into the Look and Feel table (does not have to be exact, can be "fuzzy")

bool

force

no longer used

None

**RETURN**

None

[Back](./_Elements)
