# Sizer
Note that while the Sizer is an element, it is implemented using a function and doesn't have the normal set of element methods.

This element is used to add more space.... more size...to a Container Element or a Window. They are often better to use than hard-coded sizes on the containers typically.

"Pushes" out the size of whatever it is placed inside of. This includes Columns, Frames, Tabs and Windows

```
Sizer(h_pixels = 0, v_pixels = 0)
```

Parameter Descriptions:

Type

Name

Meaning

int

h_pixels

number of horizontal pixels

int

v_pixels

number of vertical pixels

(Column)

**RETURN**

(Column) A column element that has a pad setting set according to parameters

[Back](./_Elements)
