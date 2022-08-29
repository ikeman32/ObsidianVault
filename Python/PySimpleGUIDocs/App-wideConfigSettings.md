# App-wide Config Settings
Sets the icon which will be used any time a window is created if an icon is not provided when the window is created.

```
set_global_icon(icon)
```

Parameter Descriptions:

| Type         | Name | Meaning                                   |
| ------------ | ---- | ----------------------------------------- |
| bytes or str | icon | Either a Base64 byte string or a filename |

```python
set_options(icon = None,
    button_color = None,
    element_size = (None, None),
    button_element_size = (None, None),
    margins = (None, None),
    element_padding = (None, None),
    auto_size_text = None,
    auto_size_buttons = None,
    font = None,
    border_width = None,
    slider_border_width = None,
    slider_relief = None,
    slider_orientation = None,
    autoclose_time = None,
    message_box_line_width = None,
    progress_meter_border_depth = None,
    progress_meter_style = None,
    progress_meter_relief = None,
    progress_meter_color = None,
    progress_meter_size = None,
    text_justification = None,
    background_color = None,
    element_background_color = None,
    text_element_background_color = None,
    input_elements_background_color = None,
    input_text_color = None,
    scrollbar_color = None,
    text_color = None,
    element_text_color = None,
    debug_win_size = (None, None),
    window_location = (None, None),
    error_button_color = (None, None),
    tooltip_time = None,
    tooltip_font = None,
    use_ttk_buttons = None,
    ttk_theme = None,
    suppress_error_popups = None,
    suppress_raise_key_errors = None,
    suppress_key_guessing = None,
    warn_button_key_duplicates = False,
    enable_treeview_869_patch = None,
    enable_mac_notitlebar_patch = None,
    use_custom_titlebar = None,
    titlebar_background_color = None,
    titlebar_text_color = None,
    titlebar_font = None,
    titlebar_icon = None,
    user_settings_path = None,
    pysimplegui_settings_path = None,
    pysimplegui_settings_filename = None,
    keep_on_top = None,
    dpi_awareness = None,
    scaling = None,
    disable_modal_windows = None,
    force_modal_windows = None,
    tooltip_offset = (None, None),
    sbar_trough_color = None,
    sbar_background_color = None,
    sbar_arrow_color = None,
    sbar_width = None,
    sbar_arrow_width = None,
    sbar_frame_color = None,
    sbar_relief = None,
    alpha_channel = None,
    hide_window_when_creating = None)
```

Parameter Descriptions:

| Type         | Name | Meaning                                                                                                                                                                                                      |
| ------------ | ---- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| bytes or str | icon | Can be either a filename or Base64 value. For Windows if filename, it MUST be ICO format. For Linux, must NOT be ICO. Most portable is to use a Base64 of a PNG file. This works universally across all OS's |
|(str, str) or str|button_color|Color of the button (text, background)|
|(int, int)|element_size|element size (width, height) in characters|
|(int, int)|button_element_size|Size of button|
|(int, int)|margins|(left/right, top/bottom) tkinter margins around outsize. Amount of pixels to leave inside the window's frame around the edges before your elements are shown.|
|(int, int or (int, int),(int,int))|element_padding|Default amount of padding to put around elements in window (left/right, top/bottom) or ((left, right), (top, bottom))|
|bool|auto_size_text|True if the Widget should be shrunk to exactly fit the number of chars to show|
|bool|auto_size_buttons|True if Buttons in this Window should be sized to exactly fit the text on this.|
|(str or (str, int[, str]) or None)|font|specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike|
|int|border_width|width of border around element|
|int|slider_border_width|Width of the border around sliders|
|str|slider_relief|Type of relief to use for sliders|
|???|slider_orientation|???|
|???|autoclose_time|???|
|???|message_box_line_width|???|
|???|progress_meter_border_depth|???|
|???|progress_meter_style|You can no longer set a progress bar style. All ttk styles must be the same for the window|
|???|progress_meter_relief||
|???|progress_meter_color|???|
|???|progress_meter_size|???|
|'left' or 'right' or 'center'|text_justification|Default text justification for all Text Elements in window|
|str|background_color|color of background|
|str|element_background_color|element background color|
|str|text_element_background_color|text element background color|
|str|input_elements_background_color|Default color to use for the background of input elements|
|str|input_text_color|Default color to use for the text for Input elements|
|str|scrollbar_color|Default color to use for the slider trough|
|str|text_color|color of the text|
|str|element_text_color|Default color to use for Text elements|
|(int, int)|debug_win_size|window size|
|(int, int) or None|window_location|Default location to place windows. Not setting will center windows on the display|
|???|error_button_color|(Default = (None))|
|int|tooltip_time|time in milliseconds to wait before showing a tooltip. Default is 400ms|
|str or Tuple[str, int] or Tuple[str, int, str]|tooltip_font|font to use for all tooltips|
|bool|use_ttk_buttons|if True will cause all buttons to be ttk buttons|
|str|ttk_theme|Theme to use with ttk widgets. Choices (on Windows) include - 'default', 'winnative', 'clam', 'alt', 'classic', 'vista', 'xpnative'|
|bool|suppress_error_popups|If True then error popups will not be shown if generated internally to PySimpleGUI|
|bool|suppress_raise_key_errors|If True then key errors won't be raised (you'll still get popup error)|
|bool|suppress_key_guessing|If True then key errors won't try and find closest matches for you|
|bool|warn_button_key_duplicates|If True then duplicate Button Keys generate warnings (not recommended as they're expected)|
|bool|enable_treeview_869_patch|If True, then will use the treeview color patch for tk 8.6.9|
|bool|enable_mac_notitlebar_patch|If True then Windows with no titlebar use an alternative technique when tkinter version < 8.6.10|
|bool|use_custom_titlebar|If True then a custom titlebar is used instead of the normal system titlebar|
|str or None|titlebar_background_color|If custom titlebar indicated by use_custom_titlebar, then use this as background color|
|str or None|titlebar_text_color|If custom titlebar indicated by use_custom_titlebar, then use this as text color|
|(str or (str, int[, str]) or None) or None|titlebar_font|If custom titlebar indicated by use_custom_titlebar, then use this as title font|
|bytes or str|titlebar_icon|If custom titlebar indicated by use_custom_titlebar, then use this as the icon (file or base64 bytes)|
|str|user_settings_path|default path for user_settings API calls. Expanded with os.path.expanduser so can contain ~ to represent user|
|str|pysimplegui_settings_path|default path for the global PySimpleGUI user_settings|
|str|pysimplegui_settings_filename|default filename for the global PySimpleGUI user_settings|
|bool|keep_on_top|If True then all windows will automatically be set to keep_on_top=True|
|bool|dpi_awareness|If True then will turn on DPI awareness (Windows only at the moment)|
|float|scaling|Sets the default scaling for all windows including popups, etc.|
|bool|disable_modal_windows|If True then all windows, including popups, will not be modal windows (unless they've been set to FORCED using another option)|
|bool|force_modal_windows|If True then all windows will be modal (the disable option will be ignored... all windows will be forced to be modal)|
|((None, None) or (int, int))|tooltip_offset|Offset to use for tooltips as a tuple. These values will be added to the mouse location when the widget was entered.|
|str|sbar_trough_color|Scrollbar color of the trough|
|str|sbar_background_color|Scrollbar color of the background of the arrow buttons at the ends AND the color of the "thumb" (the thing you grab and slide). Switches to arrow color when mouse is over|
|str|sbar_arrow_color|Scrollbar color of the arrow at the ends of the scrollbar (it looks like a button). Switches to background color when mouse is over|
|int|sbar_width|Scrollbar width in pixels|
|int|sbar_arrow_width|Scrollbar width of the arrow on the scrollbar. It will potentially impact the overall width of the scrollbar|
|str|sbar_frame_color|Scrollbar Color of frame around scrollbar (available only on some ttk themes)|
|str|sbar_relief|Scrollbar relief that will be used for the "thumb" of the scrollbar (the thing you grab that slides). Should be a constant that is defined at starting with "RELIEF_" - RELIEF_RAISED, RELIEF_SUNKEN, RELIEF_FLAT, RELIEF_RIDGE, RELIEF_GROOVE, RELIEF_SOLID|
|return: None|alpha_channel Default alpha channel to be used on all windows|type alpha_channel (float) :param hide_window_when_creating If True then alpha will be set to 0 while a window is made and moved to location indicated|
|None|**RETURN**|None|

### Non PEP8 versions

Sets the icon which will be used any time a window is created if an icon is not provided when the window is created.

```
SetGlobalIcon(icon)
```

Parameter Descriptions:

| Type         | Name | Meaning                                   |
| ------------ | ---- | ----------------------------------------- |
| bytes or str | icon | Either a Base64 byte string or a filename |

```
SetOptions(icon = None,
    button_color = None,
    element_size = (None, None),
    button_element_size = (None, None),
    margins = (None, None),
    element_padding = (None, None),
    auto_size_text = None,
    auto_size_buttons = None,
    font = None,
    border_width = None,
    slider_border_width = None,
    slider_relief = None,
    slider_orientation = None,
    autoclose_time = None,
    message_box_line_width = None,
    progress_meter_border_depth = None,
    progress_meter_style = None,
    progress_meter_relief = None,
    progress_meter_color = None,
    progress_meter_size = None,
    text_justification = None,
    background_color = None,
    element_background_color = None,
    text_element_background_color = None,
    input_elements_background_color = None,
    input_text_color = None,
    scrollbar_color = None,
    text_color = None,
    element_text_color = None,
    debug_win_size = (None, None),
    window_location = (None, None),
    error_button_color = (None, None),
    tooltip_time = None,
    tooltip_font = None,
    use_ttk_buttons = None,
    ttk_theme = None,
    suppress_error_popups = None,
    suppress_raise_key_errors = None,
    suppress_key_guessing = None,
    warn_button_key_duplicates = False,
    enable_treeview_869_patch = None,
    enable_mac_notitlebar_patch = None,
    use_custom_titlebar = None,
    titlebar_background_color = None,
    titlebar_text_color = None,
    titlebar_font = None,
    titlebar_icon = None,
    user_settings_path = None,
    pysimplegui_settings_path = None,
    pysimplegui_settings_filename = None,
    keep_on_top = None,
    dpi_awareness = None,
    scaling = None,
    disable_modal_windows = None,
    force_modal_windows = None,
    tooltip_offset = (None, None),
    sbar_trough_color = None,
    sbar_background_color = None,
    sbar_arrow_color = None,
    sbar_width = None,
    sbar_arrow_width = None,
    sbar_frame_color = None,
    sbar_relief = None,
    alpha_channel = None,
    hide_window_when_creating = None)
```

Parameter Descriptions:

| Type                                           | Name                            | Meaning                                                                                                                                                                                                      |
| ---------------------------------------------- | ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| bytes or str                                   | icon                            | Can be either a filename or Base64 value. For Windows if filename, it MUST be ICO format. For Linux, must NOT be ICO. Most portable is to use a Base64 of a PNG file. This works universally across all OS's |
| (str, str) or str                              | button_color                    | Color of the button (text, background)                                                                                                                                                                       |
| (int, int)                                     | element_size                    | element size (width, height) in characters                                                                                                                                                                   |
| (int, int)                                     | button_element_size             | Size of button                                                                                                                                                                                               |
| (int, int)                                     | margins                         | (left/right, top/bottom) tkinter margins around outsize. Amount of pixels to leave inside the window's frame around the edges before your elements are shown.                                                |
| (int, int or (int, int),(int,int))             | element_padding                 | Default amount of padding to put around elements in window (left/right, top/bottom) or ((left, right), (top, bottom))                                                                                        |
| bool                                           | auto_size_text                  | True if the Widget should be shrunk to exactly fit the number of chars to show                                                                                                                               |
| bool                                           | auto_size_buttons               | True if Buttons in this Window should be sized to exactly fit the text on this.                                                                                                                              |
| (str or (str, int[, str]) or None)             | font                            | specifies the font family, size, etc. Tuple or Single string format 'name size styles'. Styles: italic * roman bold normal underline overstrike                                                              |
| int                                            | border_width                    | width of border around element                                                                                                                                                                               |
| int                                            | slider_border_width             | Width of the border around sliders                                                                                                                                                                           |
| str                                            | slider_relief                   | Type of relief to use for sliders                                                                                                                                                                            |
| ???                                            | slider_orientation              | ???                                                                                                                                                                                                          |
| ???                                            | autoclose_time                  | ???                                                                                                                                                                                                          |
| ???                                            | message_box_line_width          | ???                                                                                                                                                                                                          |
| ???                                            | progress_meter_border_depth     | ???                                                                                                                                                                                                          |
| ???                                            | progress_meter_style            | You can no longer set a progress bar style. All ttk styles must be the same for the window                                                                                                                   |
| ???                                            | progress_meter_relief           |                                                                                                                                                                                                              |
| ???                                            | progress_meter_color            | ???                                                                                                                                                                                                          |
| ???                                            | progress_meter_size             | ???                                                                                                                                                                                                          |
| 'left' or 'right' or 'center'                  | text_justification              | Default text justification for all Text Elements in window                                                                                                                                                   |
| str                                            | background_color                | color of background                                                                                                                                                                                          |
| str                                            | element_background_color        | element background color                                                                                                                                                                                     |
| str                                            | text_element_background_color   | text element background color                                                                                                                                                                                |
| str                                            | input_elements_background_color | Default color to use for the background of input elements                                                                                                                                                    |
| str                                            | input_text_color                | Default color to use for the text for Input elements                                                                                                                                                         |
| str                                            | scrollbar_color                 | Default color to use for the slider trough                                                                                                                                                                   |
| str                                            | text_color                      | color of the text                                                                                                                                                                                            |
| str                                            | element_text_color              | Default color to use for Text elements                                                                                                                                                                       |
| (int, int)                                     | debug_win_size                  | window size                                                                                                                                                                                                  |
| (int, int) or None                             | window_location                 | Default location to place windows. Not setting will center windows on the display                                                                                                                            |
| ???                                            | error_button_color              | (Default = (None))                                                                                                                                                                                           |
| int                                            | tooltip_time                    | time in milliseconds to wait before showing a tooltip. Default is 400ms                                                                                                                                      |
| str or Tuple[str, int] or Tuple[str, int, str] | tooltip_font                    | font to use for all tooltips                                                                                                                                                                                 |
| bool                                           | use_ttk_buttons                 | if True will cause all buttons to be ttk buttons                                                                                                                                                             |
| str                                            | ttk_theme                       | Theme to use with ttk widgets. Choices (on Windows) include - 'default', 'winnative', 'clam', 'alt', 'classic', 'vista', 'xpnative'                                                                          |
| bool                                           | suppress_error_popups           | If True then error popups will not be shown if generated internally to PySimpleGUI                                                                                                                           |
| bool                                           | suppress_raise_key_errors       | If True then key errors won't be raised (you'll still get popup error)                                                                                                                                       |
| bool                                           | suppress_key_guessing           | If True then key errors won't try and find closest matches for you                                                                                                                                           |
| bool                                           | warn_button_key_duplicates      | If True then duplicate Button Keys generate warnings (not recommended as they're expected)                                                                                                                   |
| bool                                           | enable_treeview_869_patch       | If True, then will use the treeview color patch for tk 8.6.9                                                                                                                                                 |
| bool                                           | enable_mac_notitlebar_patch     | If True then Windows with no titlebar use an alternative technique when tkinter version < 8.6.10                                                                                                             |
| bool                                           | use_custom_titlebar             | If True then a custom titlebar is used instead of the normal system titlebar                                                                                                                                 |
| str or None                                    | titlebar_background_color       | If custom titlebar indicated by use_custom_titlebar, then use this as background color                                                                                                                       |
| str or None                                    | titlebar_text_color             | If custom titlebar indicated by use_custom_titlebar, then use this as text color                                                                                                                             |
| (str or (str, int[, str]) or None) or None     | titlebar_font                   | If custom titlebar indicated by use_custom_titlebar, then use this as title font                                                                                                                             |
| bytes or str                                   | titlebar_icon                   | If custom titlebar indicated by use_custom_titlebar, then use this as the icon (file or base64 bytes)                                                                                                        |
| str                                            | user_settings_path              | default path for user_settings API calls. Expanded with os.path.expanduser so can contain ~ to represent user                                                                                                |
| str                                            | pysimplegui_settings_path       | default path for the global PySimpleGUI user_settings                                                                                                                                                        |
| str                                            | pysimplegui_settings_filename   | default filename for the global PySimpleGUI user_settings                                                                                                                                                    |
| bool                                           | keep_on_top                     | If True then all windows will automatically be set to keep_on_top=True                                                                                                                                       |
| bool                                           | dpi_awareness                   | If True then will turn on DPI awareness (Windows only at the moment)                                                                                                                                         |
| float                                          | scaling                         | Sets the default scaling for all windows including popups, etc.                                                                                                                                              |
| bool                                           | disable_modal_windows           | If True then all windows, including popups, will not be modal windows (unless they've been set to FORCED using another option)                                                                               |
| bool                                           | force_modal_windows             | If True then all windows will be modal (the disable option will be ignored... all windows will be forced to be modal)                                                                                        |
| ((None, None) or (int, int))                   | tooltip_offset                  | Offset to use for tooltips as a tuple. These values will be added to the mouse location when the widget was entered.                                                                                         |
| str                                            | sbar_trough_color               | Scrollbar color of the trough                                                                                                                                                                                |
| str                                            | sbar_background_color           | Scrollbar color of the background of the arrow buttons at the ends AND the color of the "thumb" (the thing you grab and slide). Switches to arrow color when mouse is over|
|str|sbar_arrow_color|Scrollbar color of the arrow at the ends of the scrollbar (it looks like a button). Switches to background color when mouse is over|
|int|sbar_width|Scrollbar width in pixels|
|int|sbar_arrow_width|Scrollbar width of the arrow on the scrollbar. It will potentially impact the overall width of the scrollbar|
|str|sbar_frame_color|Scrollbar Color of frame around scrollbar (available only on some ttk themes)|
|str|sbar_relief|Scrollbar relief that will be used for the "thumb" of the scrollbar (the thing you grab that slides). Should be a constant that is defined at starting with "RELIEF_" - RELIEF_RAISED, RELIEF_SUNKEN, RELIEF_FLAT, RELIEF_RIDGE, RELIEF_GROOVE, RELIEF_SOLID|
|return: None|alpha_channel Default alpha channel to be used on all windows|type alpha_channel (float) :param hide_window_when_creating If True then alpha will be set to 0 while a window is made and moved to location indicated|
|None|**RETURN**|None|


[Back](./_Elements)