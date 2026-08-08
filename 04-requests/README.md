# 🌐 Requests Module

The **requests** module is a popular Python library used to send HTTP requests. It allows you to interact with web servers and APIs.

---

## 📥 Installation

```bash
pip install requests
```

---

## 📦 Import

```python
import requests
```

---

## 🔹 GET Request

```python
import requests

r = requests.get("https://httpbin.org/get")

print(r.status_code)
print(r.text)
```

---

## 🔹 POST Request

```python
import requests

data = {
    "name": "John",
    "age": 20
}

r = requests.post("https://httpbin.org/post", json=data)

print(r.status_code)
print(r.json())
```

---

## 🔹 PUT Request

```python
requests.put("https://httpbin.org/put", json=data)
```

Updates an existing resource.

---

## 🔹 PATCH Request

```python
requests.patch("https://httpbin.org/patch", json=data)
```

Updates part of a resource.

---

## 🔹 DELETE Request

```python
requests.delete("https://httpbin.org/delete")
```

Deletes a resource.

---

## 📄 Response Attributes

| Attribute | Description |
|-----------|-------------|
| `r.status_code` | HTTP status code |
| `r.text` | Response as text |
| `r.json()` | Response as JSON |
| `r.headers` | Response headers |
| `r.cookies` | Cookies sent by server |
| `r.url` | Final URL |

---

## 📨 Sending Parameters

```python
params = {
    "name": "John",
    "age": 20
}

r = requests.get("https://httpbin.org/get", params=params)
```

---

## 📤 Sending Form Data

```python
data = {
    "username": "admin",
    "password": "1234"
}

requests.post("https://httpbin.org/post", data=data)
```

---

## 📦 Sending JSON Data

```python
data = {
    "name": "John",
    "age": 20
}

requests.post("https://httpbin.org/post", json=data)
```

---

## 📑 Custom Headers

```python
headers = {
    "User-Agent": "MyPythonScript"
}

requests.get("https://httpbin.org/get", headers=headers)
```

---

## 🍪 Cookies

```python
cookies = {
    "session": "abc123"
}

requests.get("https://httpbin.org/cookies", cookies=cookies)
```

---

## ⏳ Timeout

```python
requests.get("https://httpbin.org/delay/10", timeout=5)
```

Raises an exception if the server doesn't respond within 5 seconds.

---

## ⚠️ Exception Handling

```python
import requests

try:
    r = requests.get("https://httpbin.org/get", timeout=5)
except requests.exceptions.RequestException as e:
    print(e)
```

---

## 📝 Common HTTP Status Codes

| Code | Meaning |
|------|---------|
| 200 | OK |
| 201 | Created |
| 204 | No Content |
| 400 | Bad Request |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal Server Error |

---

## ✅ Key Points

- Used for sending HTTP requests.
- Supports REST APIs.
- Can send parameters, headers, cookies, files, and JSON data.
