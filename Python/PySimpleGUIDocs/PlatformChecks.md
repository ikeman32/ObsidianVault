# Platform Checks
hese are simple functions you can use that return a boolean True if sys.platform matches the platform. Saves you the trouble of importing sys and then looking up the values for sys.platform.

Determines the OS is Linux by using sys.platform

Returns True if Linux

```
running_linux()
```

Parameter Descriptions:

Type

Name

Meaning

(bool)

**RETURN**

True if sys.platform indicates running Linux

Determines the OS is Mac by using sys.platform

Returns True if Mac

```
running_mac()
```

Parameter Descriptions:

Type

Name

Meaning

(bool)

**RETURN**

True if sys.platform indicates running Mac

A special case for Trinket. Checks both the OS and the number of environment variables Currently, Trinket only has ONE environment variable. This fact is used to figure out if Trinket is being used.

Returns True if "Trinket" (in theory)

```
running_trinket()
```

Parameter Descriptions:

Type

Name

Meaning

(bool)

**RETURN**

True if sys.platform indicates Linux and the number of environment variables is 1

Determines the OS is Windows by using sys.platform

Returns True if Windows

```
running_windows()
```

Parameter Descriptions:

Type

Name

Meaning

(bool)

**RETURN**

True if sys.platform indicates running Windows

[Back](./_Elements)
