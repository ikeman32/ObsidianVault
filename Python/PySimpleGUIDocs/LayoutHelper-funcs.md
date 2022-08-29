# Layout Helper Functions
Pin's an element provided into a layout so that when it's made invisible and visible again, it will be in the correct place. Otherwise it will be placed at the end of its containing window/column.

The element you want to pin is the element that you'll be making visibile/invisible.

The pin helper function also causes containers to shrink to fit the contents correct after something inside has changed visiblity. Note that setting a hardcoded size on your window can impact this ability to shrink.

```
pin(elem,
    vertical_alignment = None,
    shrink = True,
    expand_x = None,
    expand_y = None)
```

Parameter Descriptions:

Type

Name

Meaning

Element

elem

the element to put into the layout

str or None

vertical_alignment

Aligns elements vertically. 'top', 'center', 'bottom'. Can be shortened to 't', 'c', 'b'

bool

shrink

If True, then the space will shrink down to a single pixel when hidden. False leaves the area large and blank

bool

expand_x

If True/False the value will be passed to the Column Elements used to make this feature

bool

expand_y

If True/False the value will be passed to the Column Elements used to make this feature

Column

**RETURN**

A column element containing the provided element

Align an element or a row of elements to the bottom of the row that contains it

```
vbottom(elem_or_row,
    expand_x = None,
    expand_y = None,
    background_color = None)
```

Parameter Descriptions:

Type

Name

Meaning

Element or List[Element] or Tuple[Element]

elem_or_row

the element or row of elements

bool

expand_x

If True/False the value will be passed to the Column Elements used to make this feature

bool

expand_y

If True/False the value will be passed to the Column Elements used to make this feature

str or None

background_color

Background color for container that is used by vcenter to do the alignment

Column or List[Column]

**RETURN**

A column element containing the provided element aligned to the bottom or list of elements (a row)

Align an element or a row of elements to the center of the row that contains it

```
vcenter(elem_or_row,
    expand_x = None,
    expand_y = None,
    background_color = None)
```

Parameter Descriptions:

Type

Name

Meaning

Element or List[Element] or Tuple[Element]

elem_or_row

the element or row of elements

bool

expand_x

If True/False the value will be passed to the Column Elements used to make this feature

bool

expand_y

If True/False the value will be passed to the Column Elements used to make this feature

str or None

background_color

Background color for container that is used by vcenter to do the alignment

Column or List[Column]

**RETURN**

A column element containing the provided element aligned to the center or list of elements (a row)

Align an element or a row of elements to the top of the row that contains it

```
vtop(elem_or_row,
    expand_x = None,
    expand_y = None,
    background_color = None)
```

Parameter Descriptions:

Type

Name

Meaning

Element or List[Element] or Tuple[Element]

elem_or_row

the element or row of elements

bool

expand_x

If True/False the value will be passed to the Column Elements used to make this feature

bool

expand_y

If True/False the value will be passed to the Column Elements used to make this feature

str or None

background_color

Background color for container that is used by vtop to do the alignment

Column or List[Column]

**RETURN**

A column element containing the provided element aligned to the top or list of elements (a row)

[Back](./_Elements)
