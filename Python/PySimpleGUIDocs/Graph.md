# Graph
```
Creates an area for you to draw on.  The MAGICAL property this Element has is that you interact
with the element using your own coordinate system.  This is an important point!!  YOU define where the location
is for (0,0).  Want (0,0) to be in the middle of the graph like a math 4-quadrant graph?  No problem!  Set your
lower left corner to be (-100,-100) and your upper right to be (100,100) and you've got yourself a graph with
(0,0) at the center.
One of THE coolest of the Elements.
You can also use float values. To do so, be sure and set the float_values parameter.
Mouse click and drag events are possible and return the (x,y) coordinates of the mouse
Drawing primitives return an "id" that is referenced when you want to operation on that item (e.g. to erase it)
```

```
Graph(canvas_size,
    graph_bottom_left,
    graph_top_right,
    background_color = None,
    pad = None,
    p = None,
    change_submits = False,
    drag_submits = False,
    enable_events = False,
    motion_events = False,
    key = None,
    k = None,
    tooltip = None,
    right_click_menu = None,
    expand_x = False,
    expand_y = False,
    visible = True,
    float_values = False,
    border_width = 0,
    metadata = None)
```

Parameter Descriptions:

Type

Name

Meaning

(int, int)

canvas_size

size of the canvas area in pixels

(int, int)

graph_bottom_left

(x,y) The bottoms left corner of your coordinate system

(int, int)

graph_top_right

(x,y) The top right corner of your coordinate system

str

background_color

background color of the drawing area

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

pad

Amount of padding to put around element in pixels (left/right, top/bottom) or ((left, right), (top, bottom)) or an int. If an int, then it's converted into a tuple (int, int)

(int, int or (int, int),(int,int) or int,(int,int)) or ((int, int),int) or int

p

Same as pad parameter. It's an alias. If EITHER of them are set, then the one that's set will be used. If BOTH are set, pad will be used

bool

change_submits

* DEPRICATED DO NOT USE. Use `enable_events` instead

bool

drag_submits

if True and Events are enabled for the Graph, will report Events any time the mouse moves while button down. When the mouse button is released, you'll get an event = graph key + '+UP' (if key is a string.. if not a string, it'll be made into a tuple)

bool

enable_events

If True then clicks on the Graph are immediately reported as an event. Use this instead of change_submits

bool

motion_events

If True then if no button is down and the mouse is moved, an event is generated with key = graph key + '+MOVE' (if key is a string, it not a string then a tuple is returned)

str or int or tuple or object

key

Value that uniquely identifies this element from all other elements. Used when Finding an element or in return values. Must be unique to the window

str or int or tuple or object

k

Same as the Key. You can use either k or key. Which ever is set will be used.

str

tooltip

text, that will appear when mouse hovers over the element

List[List[ List[str] or str ]]

right_click_menu

A list of lists of Menu items to show when this element is right clicked. See user docs for exact format.

bool

expand_x

If True the element will automatically expand in the X direction to fill available space

bool

expand_y

If True the element will automatically expand in the Y direction to fill available space

bool

visible

set visibility state of the element (Default = True)

bool

float_values

If True x,y coordinates are returned as floats, not ints

int

border_width

width of border around element in pixels. Not normally used for Graph Elements

Any

metadata

User metadata that can be set to ANYTHING

### Update

Changes some of the settings for the Graph Element. Must call `Window.Read` or `Window.Finalize` prior

Changes will not be visible in your window until you call window.read or window.refresh.

If you change visibility, your element may MOVE. If you want it to remain stationary, use the "layout helper" function "pin" to ensure your element is "pinned" to that location in your layout so that it returns there when made visible.

```
Update(background_color = None, visible = None)
```

Parameter Descriptions:

Type

Name

Meaning

???

background_color

color of background

bool

visible

control visibility of element

### bind

Used to add tkinter events to an Element. The tkinter specific data is in the Element's member variable user_bind_event

```
bind(bind_string,
    key_modifier,
    propagate = True)
```

Parameter Descriptions:

Type

Name

Meaning

str

bind_string

The string tkinter expected in its bind function

str

key_modifier

Additional data to be added to the element's key when event is returned

bool

propagate

If True then tkinter will be told to propagate the event to the element

### block_focus

Enable or disable the element from getting focus by using the keyboard. If the block parameter is True, then this element will not be given focus by using the keyboard to go from one element to another. You CAN click on the element and utilize it.

```
block_focus(block = True)
```

Parameter Descriptions:

Type

Name

Meaning

bool

block

if True the element will not get focus via the keyboard

### bring_figure_to_front

Changes Z-order of figures on the Graph. Brings the indicated figure to the front of all other drawn figures

```
bring_figure_to_front(figure)
```

Parameter Descriptions:

Type

Name

Meaning

int

figure

value returned by tkinter when creating the figure / drawing

### change_coordinates

Changes the corrdinate system to a new one. The same 2 points in space are used to define the coorinate system - the bottom left and the top right values of your graph.

```
change_coordinates(graph_bottom_left, graph_top_right)
```

Parameter Descriptions:

Type

Name

Meaning

(int, int) (x,y)

graph_bottom_left

The bottoms left corner of your coordinate system

(int, int) (x,y)

graph_top_right

The top right corner of your coordinate system

### delete_figure

Remove from the Graph the figure represented by id. The id is given to you anytime you call a drawing primitive

```
delete_figure(id)
```

Parameter Descriptions:

Type

Name

Meaning

int

id

the id returned to you when calling one of the drawing methods

### draw_arc

Draws different types of arcs. Uses a "bounding box" to define location

```
draw_arc(top_left,
    bottom_right,
    extent,
    start_angle,
    style = None,
    arc_color = "black",
    line_width = 1,
    fill_color = None)
```

Parameter Descriptions:

Type

Name

Meaning

(int, int) or Tuple[float, float]

top_left

the top left point of bounding rectangle

(int, int) or Tuple[float, float]

bottom_right

the bottom right point of bounding rectangle

float

extent

Andle to end drawing. Used in conjunction with start_angle

float

start_angle

Angle to begin drawing. Used in conjunction with extent

str

style

Valid choices are One of these Style strings- 'pieslice', 'chord', 'arc', 'first', 'last', 'butt', 'projecting', 'round', 'bevel', 'miter'

str

arc_color

color to draw arc with

str

fill_color

color to fill the area

int or None

**RETURN**

id returned from tkinter that you'll need if you want to manipulate the arc

### draw_circle

Draws a circle, cenetered at the location provided. Can set the fill and outline colors

```
draw_circle(center_location,
    radius,
    fill_color = None,
    line_color = "black",
    line_width = 1)
```

Parameter Descriptions:

Type

Name

Meaning

(int, int) or Tuple[float, float]

center_location

Center location using USER'S coordinate system

int or float

radius

Radius in user's coordinate values.

str

fill_color

color of the point to draw

str

line_color

color of the outer line that goes around the circle (sorry, can't set thickness)

int

line_width

width of the line around the circle, the outline, in pixels

int or None

**RETURN**

id returned from tkinter that you'll need if you want to manipulate the circle

### draw_image

Places an image onto your canvas. It's a really important method for this element as it enables so much

```
draw_image(filename = None,
    data = None,
    location = (None, None))
```

Parameter Descriptions:

Type

Name

Meaning

str

filename

if image is in a file, path and filename for the image. (GIF and PNG only!)

str or bytes

data

if image is in Base64 format or raw? format then use instead of filename

(int, int) or Tuple[float, float]

location

the (x,y) location to place image's top left corner

int or None

**RETURN**

id returned from tkinter that you'll need if you want to manipulate the image

### draw_line

Draws a line from one point to another point using USER'S coordinates. Can set the color and width of line

```
draw_line(point_from,
    point_to,
    color = "black",
    width = 1)
```

Parameter Descriptions:

Type

Name

Meaning

(int, int) or Tuple[float, float]

point_from

Starting point for line

(int, int) or Tuple[float, float]

point_to

Ending point for line

str

color

Color of the line

int

width

width of line in pixels

int or None

**RETURN**

id returned from tktiner or None if user closed the window. id is used when you

### draw_oval

Draws an oval based on coordinates in user coordinate system. Provide the location of a "bounding rectangle"

```
draw_oval(top_left,
    bottom_right,
    fill_color = None,
    line_color = None,
    line_width = 1)
```

Parameter Descriptions:

Type

Name

Meaning

(int, int) or Tuple[float, float]

top_left

the top left point of bounding rectangle

(int, int) or Tuple[float, float]

bottom_right

the bottom right point of bounding rectangle

str

fill_color

color of the interrior

str

line_color

color of outline of oval

int

line_width

width of the line around the oval, the outline, in pixels

int or None

**RETURN**

id returned from tkinter that you'll need if you want to manipulate the oval

### draw_point

Draws a "dot" at the point you specify using the USER'S coordinate system

```
draw_point(point,
    size = 2,
    color = "black")
```

Parameter Descriptions:

Type

Name

Meaning

(int, int) or Tuple[float, float]

point

Center location using USER'S coordinate system

int or float

size

Radius? (Or is it the diameter?) in user's coordinate values.

str

color

color of the point to draw

int or None

**RETURN**

id returned from tkinter that you'll need if you want to manipulate the point

### draw_polygon

Draw a polygon given list of points

```
draw_polygon(points,
    fill_color = None,
    line_color = None,
    line_width = None)
```

Parameter Descriptions:

Type

Name

Meaning

List[(int, int) or Tuple[float, float]]

points

list of points that define the polygon

str

fill_color

color of the interior

str

line_color

color of outline

int

line_width

width of the line in pixels

int or None

**RETURN**

id returned from tkinter that you'll need if you want to manipulate the rectangle

### draw_rectangle

Draw a rectangle given 2 points. Can control the line and fill colors

```
draw_rectangle(top_left,
    bottom_right,
    fill_color = None,
    line_color = None,
    line_width = None)
```

Parameter Descriptions:

Type

Name

Meaning

(int, int) or Tuple[float, float]

top_left

the top left point of rectangle

(int, int) or Tuple[float, float]

bottom_right

the bottom right point of rectangle

str

fill_color

color of the interior

str

line_color

color of outline

int

line_width

width of the line in pixels

int or None

**RETURN**

int

### draw_text

Draw some text on your graph. This is how you label graph number lines for example

```
draw_text(text,
    location,
    color = "black",
    font = None,
    angle = 0,
    text_location = "center")
```

Parameter Descriptions:

Type

Name

Meaning

Any

text

text to display

(int, int) or Tuple[float, float]

location

location to place first letter

str

color

text color

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

float

angle

Angle 0 to 360 to draw the text. Zero represents horizontal text

enum

text_location

"anchor" location for the text. Values start with TEXT_LOCATION_

int or None

**RETURN**

id returned from tkinter that you'll need if you want to manipulate the text

### erase

Erase the Graph - Removes all figures previously "drawn" using the Graph methods (e.g. DrawText)

```python
erase()
```

### expand

Causes the Element to expand to fill available space in the X and Y directions. Can specify which or both directions

```
expand(expand_x = False,
    expand_y = False,
    expand_row = True)
```

Parameter Descriptions:

Type

Name

Meaning

bool

expand_x

If True Element will expand in the Horizontal directions

bool

expand_y

If True Element will expand in the Vertical directions

bool

expand_row

If True the row containing the element will also expand. Without this your element is "trapped" within the row

### get_bounding_box

Given a figure, returns the upper left and lower right bounding box coordinates

```
get_bounding_box(figure)
```

Parameter Descriptions:

Type

Name

Meaning

object

figure

a previously drawing figure

Tuple[int, int, int, int] or Tuple[float, float, float, float]

**RETURN**

upper left x, upper left y, lower right x, lower right y

### get_figures_at_location

Returns a list of figures located at a particular x,y location within the Graph

```
get_figures_at_location(location)
```

Parameter Descriptions:

Type

Name

Meaning

(int, int) or Tuple[float, float]

location

point to check

List[int]

**RETURN**

a list of previously drawn "Figures" (returned from the drawing primitives)

### get_next_focus

Gets the next element that should get focus after this element.

`get_next_focus()`

Type

Name

Meaning

(Element)

**return**

Element that will get focus after this one

### get_previous_focus

Gets the element that should get focus previous to this element.

`get_previous_focus()`

Type

Name

Meaning

(Element)

**return**

Element that should get the focus before this one

### get_size

Return the size of an element in Pixels. Care must be taken as some elements use characters to specify their size but will return pixels when calling this get_size method.

`get_size()`

Type

Name

Meaning

(int, int)

**return**

width and height of the element

### grab_anywhere_exclude

Excludes this element from being used by the grab_anywhere feature Handy for elements like a Graph element when dragging is enabled. You want the Graph element to get the drag events instead of the window dragging.

```python
grab_anywhere_exclude()
```

### grab_anywhere_include

Includes this element in the grab_anywhere feature This will allow you to make a Multline element drag a window for example

```python
grab_anywhere_include()
```

### hide_row

Hide the entire row an Element is located on. Use this if you must have all space removed when you are hiding an element, including the row container

```python
hide_row()
```

### move

Moves the entire drawing area (the canvas) by some delta from the current position. Units are indicated in your coordinate system indicated number of ticks in your coordinate system

```
move(x_direction, y_direction)
```

Parameter Descriptions:

Type

Name

Meaning

int or float

x_direction

how far to move in the "X" direction in your coordinates

int or float

y_direction

how far to move in the "Y" direction in your coordinates

### move_figure

Moves a previously drawn figure using a "delta" from current position

```
move_figure(figure,
    x_direction,
    y_direction)
```

Parameter Descriptions:

Type

Name

Meaning

id

figure

Previously obtained figure-id. These are returned from all Draw methods

int or float

x_direction

delta to apply to position in the X direction

int or float

y_direction

delta to apply to position in the Y direction

### relocate_figure

Move a previously made figure to an arbitrary (x,y) location. This differs from the Move methods because it uses absolute coordinates versus relative for Move

```
relocate_figure(figure,
    x,
    y)
```

Parameter Descriptions:

Type

Name

Meaning

id

figure

Previously obtained figure-id. These are returned from all Draw methods

int or float

x

location on X axis (in user coords) to move the upper left corner of the figure

int or float

y

location on Y axis (in user coords) to move the upper left corner of the figure

### send_figure_to_back

Changes Z-order of figures on the Graph. Sends the indicated figure to the back of all other drawn figures

```
send_figure_to_back(figure)
```

Parameter Descriptions:

Type

Name

Meaning

int

figure

value returned by tkinter when creating the figure / drawing

### key

#### property: key

Returns key for the element. This is a READONLY property. Keys can be any hashable object (basically anything except a list... tuples are ok, but not lists)

Type

Name

Meaning

(Any)

**return**

The window's Key

### metadata

#### property: metadata

Metadata is an Element property that you can use at any time to hold any value

Type

Name

Meaning

(Any)

**return**

the current metadata value

### set_cursor

Sets the cursor for the current Element. "Cursor" is used in 2 different ways in this call. For the parameter "cursor" it's actually the mouse pointer. If you do not want any mouse pointer, then use the string "none" For the parameter "cursor_color" it's the color of the beam used when typing into an input element

```
set_cursor(cursor = None, cursor_color = None)
```

Parameter Descriptions:

Type

Name

Meaning

str

cursor

The tkinter cursor name

str

cursor_color

color to set the "cursor" to

### set_focus

Sets the current focus to be on this element

```
set_focus(force = False)
```

Parameter Descriptions:

Type

Name

Meaning

bool

force

if True will call focus_force otherwise calls focus_set

### set_size

Changes the size of an element to a specific size. It's possible to specify None for one of sizes so that only 1 of the element's dimensions are changed.

```
set_size(size = (None, None))
```

Parameter Descriptions:

Type

Name

Meaning

(int, int)

size

The size in characters, rows typically. In some cases they are pixels

### set_tooltip

Called by application to change the tooltip text for an Element. Normally invoked using the Element Object such as: window.Element('key').SetToolTip('New tip').

```
set_tooltip(tooltip_text)
```

Parameter Descriptions:

Type

Name

Meaning

str

tooltip_text

the text to show in tooltip.

### tk_canvas

#### property: tk_canvas

Returns the underlying tkiner Canvas widget

Type

Name

Meaning

(tk.Canvas)

**return**

The tkinter canvas widget

### unbind

Removes a previously bound tkinter event from an Element.

```
unbind(bind_string)
```

Parameter Descriptions:

Type

Name

Meaning

str

bind_string

The string tkinter expected in its bind function

### unhide_row

Unhides (makes visible again) the row container that the Element is located on. Note that it will re-appear at the bottom of the window / container, most likely.

```python
unhide_row()
```

### update

Changes some of the settings for the Graph Element. Must call `Window.Read` or `Window.Finalize` prior

Changes will not be visible in your window until you call window.read or window.refresh.

If you change visibility, your element may MOVE. If you want it to remain stationary, use the "layout helper" function "pin" to ensure your element is "pinned" to that location in your layout so that it returns there when made visible.

```
update(background_color = None, visible = None)
```

Parameter Descriptions:

Type

Name

Meaning

???

background_color

color of background

bool

visible

control visibility of element

### visible

#### property: visible

Returns visibility state for the element. This is a READONLY property

Type

Name

Meaning

(bool)

**return**

Visibility state for element

### widget

#### property: widget

Returns tkinter widget for the element. This is a READONLY property. The implementation is that the Widget member variable is returned. This is a backward compatible addition

Type

Name

Meaning

(tkinter.Widget)

**return**

The element's underlying tkinter widget

---

### These are non-PEP8 Compliant Methods - do NOT use

The following methods are here for backwards compatibility reference. You will find there are PEP8 versions for each of these methods. The PEP8 versions will be all lower case and have underscores.

### BringFigureToFront

Changes Z-order of figures on the Graph. Brings the indicated figure to the front of all other drawn figures

```
BringFigureToFront(figure)
```

Parameter Descriptions:

Type

Name

Meaning

int

figure

value returned by tkinter when creating the figure / drawing

### DeleteFigure

Remove from the Graph the figure represented by id. The id is given to you anytime you call a drawing primitive

```
DeleteFigure(id)
```

Parameter Descriptions:

Type

Name

Meaning

int

id

the id returned to you when calling one of the drawing methods

### DrawArc

Draws different types of arcs. Uses a "bounding box" to define location

```
DrawArc(top_left,
    bottom_right,
    extent,
    start_angle,
    style = None,
    arc_color = "black",
    line_width = 1,
    fill_color = None)
```

Parameter Descriptions:

Type

Name

Meaning

(int, int) or Tuple[float, float]

top_left

the top left point of bounding rectangle

(int, int) or Tuple[float, float]

bottom_right

the bottom right point of bounding rectangle

float

extent

Andle to end drawing. Used in conjunction with start_angle

float

start_angle

Angle to begin drawing. Used in conjunction with extent

str

style

Valid choices are One of these Style strings- 'pieslice', 'chord', 'arc', 'first', 'last', 'butt', 'projecting', 'round', 'bevel', 'miter'

str

arc_color

color to draw arc with

str

fill_color

color to fill the area

int or None

**RETURN**

id returned from tkinter that you'll need if you want to manipulate the arc

### DrawCircle

Draws a circle, cenetered at the location provided. Can set the fill and outline colors

```
DrawCircle(center_location,
    radius,
    fill_color = None,
    line_color = "black",
    line_width = 1)
```

Parameter Descriptions:

Type

Name

Meaning

(int, int) or Tuple[float, float]

center_location

Center location using USER'S coordinate system

int or float

radius

Radius in user's coordinate values.

str

fill_color

color of the point to draw

str

line_color

color of the outer line that goes around the circle (sorry, can't set thickness)

int

line_width

width of the line around the circle, the outline, in pixels

int or None

**RETURN**

id returned from tkinter that you'll need if you want to manipulate the circle

### DrawImage

Places an image onto your canvas. It's a really important method for this element as it enables so much

```
DrawImage(filename = None,
    data = None,
    location = (None, None))
```

Parameter Descriptions:

Type

Name

Meaning

str

filename

if image is in a file, path and filename for the image. (GIF and PNG only!)

str or bytes

data

if image is in Base64 format or raw? format then use instead of filename

(int, int) or Tuple[float, float]

location

the (x,y) location to place image's top left corner

int or None

**RETURN**

id returned from tkinter that you'll need if you want to manipulate the image

### DrawLine

Draws a line from one point to another point using USER'S coordinates. Can set the color and width of line

```
DrawLine(point_from,
    point_to,
    color = "black",
    width = 1)
```

Parameter Descriptions:

Type

Name

Meaning

(int, int) or Tuple[float, float]

point_from

Starting point for line

(int, int) or Tuple[float, float]

point_to

Ending point for line

str

color

Color of the line

int

width

width of line in pixels

int or None

**RETURN**

id returned from tktiner or None if user closed the window. id is used when you

### DrawOval

Draws an oval based on coordinates in user coordinate system. Provide the location of a "bounding rectangle"

```
DrawOval(top_left,
    bottom_right,
    fill_color = None,
    line_color = None,
    line_width = 1)
```

Parameter Descriptions:

Type

Name

Meaning

(int, int) or Tuple[float, float]

top_left

the top left point of bounding rectangle

(int, int) or Tuple[float, float]

bottom_right

the bottom right point of bounding rectangle

str

fill_color

color of the interrior

str

line_color

color of outline of oval

int

line_width

width of the line around the oval, the outline, in pixels

int or None

**RETURN**

id returned from tkinter that you'll need if you want to manipulate the oval

### DrawPoint

Draws a "dot" at the point you specify using the USER'S coordinate system

```
DrawPoint(point,
    size = 2,
    color = "black")
```

Parameter Descriptions:

Type

Name

Meaning

(int, int) or Tuple[float, float]

point

Center location using USER'S coordinate system

int or float

size

Radius? (Or is it the diameter?) in user's coordinate values.

str

color

color of the point to draw

int or None

**RETURN**

id returned from tkinter that you'll need if you want to manipulate the point

### DrawPolygon

Draw a polygon given list of points

```
DrawPolygon(points,
    fill_color = None,
    line_color = None,
    line_width = None)
```

Parameter Descriptions:

Type

Name

Meaning

List[(int, int) or Tuple[float, float]]

points

list of points that define the polygon

str

fill_color

color of the interior

str

line_color

color of outline

int

line_width

width of the line in pixels

int or None

**RETURN**

id returned from tkinter that you'll need if you want to manipulate the rectangle

### DrawRectangle

Draw a rectangle given 2 points. Can control the line and fill colors

```
DrawRectangle(top_left,
    bottom_right,
    fill_color = None,
    line_color = None,
    line_width = None)
```

Parameter Descriptions:

Type

Name

Meaning

(int, int) or Tuple[float, float]

top_left

the top left point of rectangle

(int, int) or Tuple[float, float]

bottom_right

the bottom right point of rectangle

str

fill_color

color of the interior

str

line_color

color of outline

int

line_width

width of the line in pixels

int or None

**RETURN**

int

### DrawText

Draw some text on your graph. This is how you label graph number lines for example

```
DrawText(text,
    location,
    color = "black",
    font = None,
    angle = 0,
    text_location = "center")
```

Parameter Descriptions:

Type

Name

Meaning

Any

text

text to display

(int, int) or Tuple[float, float]

location

location to place first letter

str

color

text color

(str or (str, int[, str]) or None)

font

specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike

float

angle

Angle 0 to 360 to draw the text. Zero represents horizontal text

enum

text_location

"anchor" location for the text. Values start with TEXT_LOCATION_

int or None

**RETURN**

id returned from tkinter that you'll need if you want to manipulate the text

### Erase

Erase the Graph - Removes all figures previously "drawn" using the Graph methods (e.g. DrawText)

```python
Erase()
```

### GetBoundingBox

Given a figure, returns the upper left and lower right bounding box coordinates

```
GetBoundingBox(figure)
```

Parameter Descriptions:

Type

Name

Meaning

object

figure

a previously drawing figure

Tuple[int, int, int, int] or Tuple[float, float, float, float]

**RETURN**

upper left x, upper left y, lower right x, lower right y

### GetFiguresAtLocation

Returns a list of figures located at a particular x,y location within the Graph

```
GetFiguresAtLocation(location)
```

Parameter Descriptions:

Type

Name

Meaning

(int, int) or Tuple[float, float]

location

point to check

List[int]

**RETURN**

a list of previously drawn "Figures" (returned from the drawing primitives)

### Move

Moves the entire drawing area (the canvas) by some delta from the current position. Units are indicated in your coordinate system indicated number of ticks in your coordinate system

```
Move(x_direction, y_direction)
```

Parameter Descriptions:

Type

Name

Meaning

int or float

x_direction

how far to move in the "X" direction in your coordinates

int or float

y_direction

how far to move in the "Y" direction in your coordinates

### MoveFigure

Moves a previously drawn figure using a "delta" from current position

```
MoveFigure(figure,
    x_direction,
    y_direction)
```

Parameter Descriptions:

Type

Name

Meaning

id

figure

Previously obtained figure-id. These are returned from all Draw methods

int or float

x_direction

delta to apply to position in the X direction

int or float

y_direction

delta to apply to position in the Y direction

### RelocateFigure

Move a previously made figure to an arbitrary (x,y) location. This differs from the Move methods because it uses absolute coordinates versus relative for Move

```
RelocateFigure(figure,
    x,
    y)
```

Parameter Descriptions:

Type

Name

Meaning

id

figure

Previously obtained figure-id. These are returned from all Draw methods

int or float

x

location on X axis (in user coords) to move the upper left corner of the figure

int or float

y

location on Y axis (in user coords) to move the upper left corner of the figure

### SendFigureToBack

Changes Z-order of figures on the Graph. Sends the indicated figure to the back of all other drawn figures

```
SendFigureToBack(figure)
```

Parameter Descriptions:

Type

Name

Meaning

int

figure

value returned by tkinter when creating the figure / drawing

### SetFocus

Sets the current focus to be on this element

```
SetFocus(force = False)
```

Parameter Descriptions:

Type

Name

Meaning

bool

force

if True will call focus_force otherwise calls focus_set

### SetTooltip

Called by application to change the tooltip text for an Element. Normally invoked using the Element Object such as: window.Element('key').SetToolTip('New tip').

```
SetTooltip(tooltip_text)
```

Parameter Descriptions:

Type

Name

Meaning

str

tooltip_text

the text to show in tooltip.

### TKCanvas

#### property: TKCanvas

Returns the underlying tkiner Canvas widget

Type

Name

Meaning

(tk.Canvas)

**return**

The tkinter canvas widget

[Back](./_Elements)
