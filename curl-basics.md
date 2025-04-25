# 🌐 curl Basics - Quick Notes

`curl` is a command-line tool used to send HTTP requests and view responses. It’s great for testing APIs, web servers, and debugging HTTP interactions.

---

## 📦 What is curl?

- Stands for **Client URL**
- Command-line tool for making **network requests**
- Supports multiple protocols: HTTP, HTTPS, FTP, etc.
- Comes pre-installed on most Unix-like systems

---

## ✅ Why Use curl?

- Test local or remote servers
- Send custom HTTP requests (GET, POST, PUT, DELETE)
- Add headers, data, or even files to requests
- Great for debugging with `-v` (verbose)

---

## 🚀 Basic Usage

|Option | Description|
|-------|------------|
|`-v` | Verbose mode (debug output)|
|`-X` | Specify HTTP method (e.g. GET, POST)|
|`-H` | Add a header to the request|
|`-d` | Send data in the request body|
|`-i` | Show response headers|


##### GET Request
```bash
curl http://localhost:4221
```

##### Verbose Output (see headers and status codes)
_Eg: Testing a local server_
```bash
curl -v http://localhost:4221
```

##### POST Request
```bash
curl -X POST http://localhost:4221
```

##### Send JSON Data
```bash
curl -X POST http://localhost:4221 \
     -H "Content-Type: application/json" \
     -d '{"name": "Alice", "age": 25}'
```

##### Add Custom Headers
```bash
curl -H "Authorization: Bearer <your_token>" http://localhost:4221
```
