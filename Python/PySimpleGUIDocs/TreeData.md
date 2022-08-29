# Tree Data  (for Tree Element)
```
Class that user fills in to represent their tree data. It's a very simple tree representation with a root "Node"
with possibly one or more children "Nodes".  Each Node contains a key, text to display, list of values to display
and an icon.  The entire tree is built using a single method, Insert.  Nothing else is required to make the tree.
```

Instantiate the object, initializes the Tree Data, creates a root node for you

```python
TreeData()
```

### Node

Contains information about the individual node in the tree

```
Node(parent,
    key,
    text,
    values,
    icon = None)
```

### insert

Inserts a node into the tree. This is how user builds their tree, by Inserting Nodes This is the ONLY user callable method in the TreeData class

```
insert(parent,
    key,
    text,
    values,
    icon = None)
```

Parameter Descriptions:

Type

Name

Meaning

Node

parent

the parent Node

str or int or tuple or object

key

Used to uniquely identify this node

str

text

The text that is displayed at this node's location

List[Any]

values

The list of values that are displayed at this node

str or bytes

icon

icon

### Insert

Inserts a node into the tree. This is how user builds their tree, by Inserting Nodes This is the ONLY user callable method in the TreeData class

```
Insert(parent,
    key,
    text,
    values,
    icon = None)
```

Parameter Descriptions:

Type

Name

Meaning

Node

parent

the parent Node

str or int or tuple or object

key

Used to uniquely identify this node

str

text

The text that is displayed at this node's location

List[Any]

values

The list of values that are displayed at this node

str or bytes

icon

icon

[Back](./_Elements)
