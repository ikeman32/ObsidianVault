# VPush (aliases include `VP` and `VStretch`)
Like the `Push` element, this is not a true element but rather a function acting like an element. It will "Push" all elements above and below away from it.

Example: If first row has a `VPush`, then your layout will be At the bottom of the container it is in. If one is on the last row, then the layout will be at the top of the container. If you use TWO `VPush`, one on the first row and one on the last row, then your layout will be centered vertically.

Acts like a Stretch element found in the Qt port. Used in a Vertical fashion.

```
VPush(background_color = None)
```

Parameter Descriptions:

Type

Name

Meaning

str

background_color

color of background may be needed because of how this is implemented

[Back](./_Elements)
