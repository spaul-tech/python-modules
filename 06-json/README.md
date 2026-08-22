# `json` Module

Notes and examples for working with Python's built-in `json` module — used to encode and decode JSON data.

## Import

```python
import json
```

---
## Core Functions

| Function | Description |
|---|---|
| `json.load(file)` | Parses JSON from a file object into a Python object |
| `json.loads(string)` | Parses JSON from a string into a Python object |
| `json.dump(obj, file)` | Writes a Python object as JSON to a file |
| `json.dumps(obj)` | Converts a Python object into a JSON-formatted string |

---
## Reading JSON

**From a file:**
```python
import json

with open("data.json", "r") as f:
    data = json.load(f)
print(data)
```

**From a string:**
```python
import json

json_string = '{"name": "Alice", "age": 25}'
data = json.loads(json_string)

print(data["name"])  # Alice
```
---
## Writing JSON

**To a file:**
```python
import json

data = {"name": "Alice", "age": 25}
with open("output.json", "w") as f:
    json.dump(data, f)
```

**To a string:**
```python
import json

data = {"name": "Alice", "age": 25}
json_string = json.dumps(data)
print(json_string)  # {"name": "Alice", "age": 25}
```
---

## Printing

```python
import json

data = {"name": "Alice", "age": 25, "skills": ["Python", "SQL"]}

print(json.dumps(data, indent=4))
```

**Output:**
```json
{
    "name": "Alice",
    "age": 25,
    "skills": [
        "Python",
        "SQL"
    ]
}
```
---

## Sorting Keys

```python
json.dumps(data, indent=4, sort_keys=True)
```
