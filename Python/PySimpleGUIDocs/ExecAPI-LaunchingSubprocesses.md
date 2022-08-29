# Exec API Launching Subprocesses
These API calls are used to launch subprocesses. You can launch Python files or any type of executable file. In these calls is where you invoke the editor and file explorer that was specified in the PySimpleGUI Global Settings.

Runs the specified command as a subprocess. By default the call is non-blocking. The function will immediately return without waiting for the process to complete running. You can use the returned Popen object to communicate with the subprocess and get the results. Returns a subprocess Popen object.

```
execute_command_subprocess(command,
    args=*<1 or N object>,
    wait = False,
    cwd = None,
    pipe_output = False,
    merge_stderr_with_stdout = True,
    stdin = None)
```

Parameter Descriptions:

Type

Name

Meaning

str

command

Filename to load settings from (and save to in the future)

Any

*args

Variable number of arguments that are passed to the program being started as command line parms

bool

wait

If True then wait for the subprocess to finish

str

cwd

Working directory to use when executing the subprocess

bool

pipe_output

If True then output from the subprocess will be piped. You MUST empty the pipe by calling execute_get_results or your subprocess will block until no longer full

bool

merge_stderr_with_stdout

If True then output from the subprocess stderr will be merged with stdout. The result is ALL output will be on stdout.

bool

stdin

Value passed to the Popen call. Defaults to subprocess.DEVNULL so that the pyinstaller created executable work correctly

(subprocess.Popen)

**RETURN**

Popen object

Runs the editor that was configured in the global settings and opens the file to a specific line number. Two global settings keys are used. '-editor program-' the command line used to startup your editor. It's set in the global settings window or by directly manipulating the PySimpleGUI settings object '-editor format string-' a string containing 3 "tokens" that describes the command that is executed

```
execute_editor(file_to_edit, line_number = None)
```

Parameter Descriptions:

Type

Name

Meaning

str

file_to_edit

the full path to the file to edit

int

line_number

optional line number to place the cursor

(subprocess.Popen) or None

**RETURN**

Popen object

The global settings has a setting called - "-explorer program-" It defines the program to run when this function is called. The optional folder paramter specified which path should be opened.

```
execute_file_explorer(folder_to_open = "")
```

Parameter Descriptions:

Type

Name

Meaning

str

folder_to_open

The path to open in the explorer program

(subprocess.Popen) or None

**RETURN**

Popen object

Returns the first filename found in a traceback that is not the nsame of this file (**file**) Used internally with the debugger for example.

```
execute_find_callers_filename()
```

Parameter Descriptions:

Type

Name

Meaning

str

**RETURN**

filename of the caller, asseumed to be the first non PySimpleGUI file

Get the text results of a previously executed execute call Returns a tuple of the strings (stdout, stderr)

```
execute_get_results(subprocess_id, timeout = None)
```

Parameter Descriptions:

Type

Name

Meaning

(subprocess.Popen)

subprocess_id

a Popen subprocess ID returned from a previous execute call

(None or float)

timeout

Time in fractions of a second to wait. Returns '','' if timeout. Default of None means wait forever

Executes a Python file. The interpreter to use is chosen based on this priority order: 1. interpreter_command paramter 2. global setting "-python command-" 3. the interpreter running running PySimpleGUI

```
execute_py_file(pyfile,
    parms = None,
    cwd = None,
    interpreter_command = None,
    wait = False,
    pipe_output = False,
    merge_stderr_with_stdout = True)
```

Parameter Descriptions:

Type

Name

Meaning

str

pyfile

the file to run

str

parms

parameters to pass on the command line

str

cwd

the working directory to use

str

interpreter_command

the command used to invoke the Python interpreter

bool

wait

the working directory to use

bool

pipe_output

If True then output from the subprocess will be piped. You MUST empty the pipe by calling execute_get_results or your subprocess will block until no longer full

bool

merge_stderr_with_stdout

If True then output from the subprocess stderr will be merged with stdout. The result is ALL output will be on stdout.

(subprocess.Popen) or None

**RETURN**

Popen object

Returns True is the subprocess ID provided is for a process that is still running

```
execute_subprocess_still_running(subprocess_id)
```

Parameter Descriptions:

Type

Name

Meaning

(subprocess.Popen)

subprocess_id

ID previously returned from Exec API calls that indicate this value is returned

bool

**RETURN**

True if the subproces is running

[Back](./_Elements)
