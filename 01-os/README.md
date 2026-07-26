# 📁 Python `os` Module

The `os` module provides a way to interact with the operating system. It is commonly used for file management, environment variables, process handling, and executing system commands.

---

## 📚 Functions Covered

| Function | Description |
|----------|-------------|
| `os.getcwd()` | Returns the current working directory. |
| `os.chdir(path)` | Changes the current working directory. |
| `os.listdir(path)` | Lists files and folders in a directory. |
| `os.mkdir(path)` | Creates a new directory. |
| `os.makedirs(path)` | Creates nested directories. |
| `os.rmdir(path)` | Removes an empty directory. |
| `os.removedirs(path)` | Removes nested empty directories. |
| `os.rename(src, dst)` | Renames a file or directory. |
| `os.remove(path)` | Deletes a file. |
| `os.path.exists(path)` | Checks if a file or directory exists. |
| `os.path.isfile(path)` | Checks whether a path is a file. |
| `os.path.isdir(path)` | Checks whether a path is a directory. |
| `os.path.join()` | Joins path components correctly for the operating system. |
| `os.path.abspath(path)` | Returns the absolute path. |
| `os.environ` | Accesses environment variables. |
| `os.getenv(name)` | Returns the value of an environment variable. |
| `os.system(command)` | Executes a system command. |


---

> **Note:** For modern file path manipulation, prefer `pathlib` over `os.path` whenever possible. It provides a cleaner and more Pythonic interface.
