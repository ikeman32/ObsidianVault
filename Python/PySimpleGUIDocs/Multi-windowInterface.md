# Multi-window Interface
Reads all windows that are "active" when the call is made. "Active" means that it's been finalized or read. If a window has not been finalized then it will not be considered an "active window"

If any of the active windows returns a value then the window and its event and values are returned.

If no windows are open, then the value (None, WIN_CLOSED, None) will be returned Since WIN_CLOSED is None, it means (None, None, None) is what's returned when no windows remain opened

```
read_all_windows(timeout = None, timeout_key = "__TIMEOUT__")
```

Parameter Descriptions:

Type

Name

Meaning

int

timeout

Time in milliseconds to delay before a returning a timeout event

Any

timeout_key

Key to return when a timeout happens. Defaults to the standard TIMEOUT_KEY

(Window, Any, Dict or List)

**RETURN**

A tuple with the (Window, event, values dictionary/list)

[Back](./_Elements)
