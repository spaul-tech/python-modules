# ⚙️ Python `subprocess` Module

The `subprocess` module allows Python to create and manage new processes. It is commonly used to execute system commands, 
run external programs, automate tasks, and capture their output.

## 📌 Common Functions

### `subprocess.run()`
Runs a command and waits for it to finish.

```python
import subprocess

subprocess.run(["ping", "google.com"])
```
---

## 📌 Useful Parameters

| Parameter | Description |
|-----------|-------------|
| `capture_output=True` | Captures both stdout and stderr |
| `text=True` | Returns output as a string instead of bytes |
| `check=True` | Raises an exception if the command fails |
| `shell=True` | Executes the command through the system shell |
| `timeout=5` | Stops the command if it exceeds the specified time |

---

## 📌 Capturing Output

```python
import subprocess

result = subprocess.run(
    ["ipconfig"],
    capture_output=True,
    text=True
)

print(result.stdout)
```

---

## 📌 Error Handling

```python
import subprocess

try:
    subprocess.run(
        ["ls", "/invalid"],
        check=True
    )
except subprocess.CalledProcessError:
    print("Command failed!")
```

---

## 📌 Timeout Example

```python
import subprocess

try:
    subprocess.run(
        ["ping", "google.com"],
        timeout=2
    )
except subprocess.TimeoutExpired:
    print("Command timed out!")
```

---

## 📌 Common Result Attributes

| Attribute | Description |
|----------|-------------|
| `stdout` | Standard output |
| `stderr` | Error output |
| `returncode` | Exit status (`0` = Success) |
| `args` | Executed command |

---

## 📌 Common Exceptions

- `subprocess.CalledProcessError`
- `subprocess.TimeoutExpired`
- `FileNotFoundError`
- `PermissionError`

---

## 📌 Common Use Cases

- Execute system commands
- Run external applications
- Automate repetitive tasks
- Capture command output
- Verify command success or failure
- Run cybersecurity tools (Nmap, Ping, Traceroute, etc.)


