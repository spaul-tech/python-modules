# 📁 Python pathlib Module

## 📌 Introduction

`pathlib` is a built-in Python module used for working with file and directory paths.
It provides an object-oriented way to handle paths instead of using traditional string-based methods.

```python
from pathlib import Path
```

---

## 🔹 Creating Paths

### Current Directory

```python
from pathlib import Path

path = Path.cwd()

print(path)
```

Output:

```
/home/kali/projects
```

---

### Creating a Path Object

```python
path = Path("test.txt")

print(path)
```

---

## 🔹 Checking Files and Directories

### Check if Path Exists

```python
path = Path("test.txt")

print(path.exists())
```

Output:

```
True
```

---

### Check File

```python
path.is_file()
```

Returns `True` if it is a file.

---

### Check Directory

```python
path.is_dir()
```

Returns `True` if it is a directory.

---

## 🔹 File Operations

## Create a File

```python
file = Path("example.txt")

file.touch()
```

Creates an empty file.

---

## Read File

```python
file = Path("example.txt")

content = file.read_text()

print(content)
```

---

## Write to File

```python
file = Path("example.txt")

file.write_text("Hello Python")
```

---

## 🔹 Directory Operations

## Create Directory

```python
folder = Path("logs")

folder.mkdir()
```

---

## Create Nested Directories

```python
folder = Path("data/logs")

folder.mkdir(parents=True)
```

---

## List Files

```python
folder = Path(".")

for file in folder.iterdir():
    print(file)
```

---

## 🔹 Searching Files

## Find Python Files

```python
path = Path(".")

for file in path.glob("*.py"):
    print(file)
```

Output:

```
scanner.py
collector.py
```

---

## Recursive Search

Search inside subdirectories:

```python
for file in Path(".").rglob("*.txt"):
    print(file)
```

---

## 🔹 Path Information

```python
file = Path("/home/kali/test.py")

print(file.name)
print(file.stem)
print(file.suffix)
```

Output:

```
test.py
test
.py
```

---

## 🔹 Joining Paths

Instead of:

```python
"folder/" + "file.txt"
```

Use:

```python
path = Path("folder") / "file.txt"

print(path)
```

Output:

```
folder/file.txt
```

---

## 🔹 Rename and Delete

## Rename File

```python
file = Path("old.txt")

file.rename("new.txt")
```

---

## Delete File

```python
file.unlink()
```

---

## 🔹 Cybersecurity Uses

`pathlib` is useful for:

- 📄 Log file collection
- 🔍 Searching suspicious files
- 📂 Automating file analysis
- 🛡️ Security tool scripting
- 📊 Organizing scan results

Example:

```python
from pathlib import Path

logs = Path("/var/log")

for file in logs.glob("*.log"):
    print(file)
```

---

# ✅ Key Functions

| Function | Purpose |
|----------|---------|
| `Path()` | Create path object |
| `cwd()` | Get current directory |
| `exists()` | Check existence |
| `is_file()` | Check file |
| `is_dir()` | Check directory |
| `mkdir()` | Create directory |
| `iterdir()` | List contents |
| `glob()` | Search files |
| `read_text()` | Read file |
| `write_text()` | Write file |
| `unlink()` | Delete file |
