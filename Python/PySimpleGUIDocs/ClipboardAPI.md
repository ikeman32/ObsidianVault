# Clipboard API
Note that this clipboard uses tkinter's clipboard. There is a known limitation that your application needs to remain running until you've pasted the contents. Managed to get around this limitation so that the clipboard stays set after you exit your application, but only have it working for Windows systems.

Gets the clipboard current value.

```
clipboard_get()
```

Parameter Descriptions:

Type

Name

Meaning

(str)

**RETURN**

The current value of the clipboard

Sets the clipboard to a specific value. IMPORTANT NOTE - Your PySimpleGUI application needs to remain running until you've pasted your clipboard. This is a tkinter limitation. A workaround was found for Windows, but you still need to stay running for Linux systems.

```
clipboard_set(new_value)
```

Parameter Descriptions:

Type

Name

Meaning

(str or bytes)

new_value

value to set the clipboard to. Will be converted to a string

[Back](./_Elements)
