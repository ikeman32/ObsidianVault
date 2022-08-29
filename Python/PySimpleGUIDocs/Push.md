# Push ## (alias include `P` and `Stretch`)
Not a true element, but a function acting like an element.

These elements `Push` and `VPush` as aliases for `Stretch` and `VStretch` and are implemented using a function rather than a class. They're not meant to be manipulated like other elements. They have a functional role in a layout that is much like the "Layout Helper Functions" (pin, vtop, etc).

The name `Stretch` originally appeared in the PySimpleGUI APIs when the PySimpleGUIQt port was added.

In the Sept 2021 time-frame, a functioning version of this element appeared in the tkinter port, along with some aliases and a vertical addition.

The PySimpleGUI documentation, demos, etc, will be using the names `Push` and `VPush`.

### Push-style Elements Use

These elements modify the placement of other elements inside of containers. As the name implies, these elements `Push` and `VPush` will "push" other elements around. `Push` works in the horizontal direction, `VPush` in the vertical.

A `Push` element will "push" elements on the row away from it. If you have 1 `Push` as the start of a row, then the row will be right-justified. If you have two `Push` elements, one as the first element and one as the last element on a row, then the row will be centered.

Acts like a Stretch element found in the Qt port. Used in a Horizontal fashion. Placing one on each side of an element will enter the element. Place one to the left and the element to the right will be right justified. See VStretch for vertical type

```
Push(background_color = None)
```

Parameter Descriptions:

Type

Name

Meaning

str

background_color

color of background may be needed because of how this is implemented

[Back](./_Elements)
