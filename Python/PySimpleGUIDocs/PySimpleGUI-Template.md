# PySimpleGUI Template

``` python,
import PySimpleGUI as sg

sg.theme('Theme Name') # Add some color

# All the stuf in the window.
layout = [
	[]
]

# Create the window
window = sg.Window('Window Title', layout)

# Even loop
while True:
	event, values = window.read()
	
	if event == sg.WINDOW_CLOSED: # If the user closes the window
		break

window.close()
```

[Back](./_Elements)
