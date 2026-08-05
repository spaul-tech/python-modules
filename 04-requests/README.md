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
