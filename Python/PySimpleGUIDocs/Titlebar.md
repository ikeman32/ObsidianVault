# Title Bar
Note that while the Titlebar is an element, it is implemented using a function.

It is actually a "compound element" that consists of several elements combined into a single Column element. See the Column element to get a list of method calls available. The function returns a Column element. This type of construct is referred to as "User Defined Elements" in the documentation and tutorials.

A custom titlebar that replaces the OS provided titlebar, thus giving you control the is not possible using the OS provided titlebar such as the color.

NOTE LINUX USERS - at the moment the minimize function is not yet working. Windows users should have no problem and it should function as a normal window would.

This titlebar is created from a row of elements that is then encapsulated into a one Column element which is what this Titlebar function returns to you.

A custom titlebar removes the margins from your window. If you want the remainder of your Window to have margins, place the layout after the Titlebar into a Column and set the pad of that Column to the dimensions you would like your margins to have.

The Titlebar is a COLUMN element. You can thus call the update method for the column and perform operations such as making the column visible/invisible

```
Titlebar(title = "",
    icon = None,
    text_color = None,
    background_color = None,
    font = None,
    key = None,
    k = None)
```

Parameter Descriptions:

Type

Name

Meaning

str or bytes or None

icon

Can be either a filename or Base64 byte string of a PNG or GIF. This is used in an Image element to create the titlebar

str

title

The "title" to show in the titlebar

str or None

text_color

Text color for titlebar

str or None

background_color

Background color for titlebar

(str or (str, int[, str]) or None)

font

Font to be used for the text and the symbols

str or int or tuple or object or None

key

Identifies an Element. Should be UNIQUE to this window.

str or int or tuple or object or None

k

Exactly the same as key. Choose one of them to use

Column

**RETURN**

A single Column element that has eveything in 1 element

[Back](./_Elements)
