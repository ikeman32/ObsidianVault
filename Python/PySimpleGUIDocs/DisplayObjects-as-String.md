# Display Objects as String
hese functions will return an object as a string that shows each of the object's member variables. They're nice to use if you want to print any Python object, not just PySimpleGUI ones.

Dumps an Object's values as a formatted string. Very nicely done. Great way to display an object's member variables in human form

```
obj_to_string(obj, extra = "    ")
```

Parameter Descriptions:

Type

Name

Meaning

Any

obj

The object to display

str

extra

extra stuff (Default value = ' ')

(str)

**RETURN**

Formatted output of the object's values

Dumps an Object's values as a formatted string. Very nicely done. Great way to display an object's member variables in human form Returns only the top-most object's variables instead of drilling down to dispolay more

```
obj_to_string_single_obj(obj)
```

Parameter Descriptions:

Type

Name

Meaning

Any

obj

The object to display

(str)

**RETURN**

Formatted output of the object's values

[Back](./_Elements)
