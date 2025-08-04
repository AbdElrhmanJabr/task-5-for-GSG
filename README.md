# task-5-for-GSG

# Node.js Core Modules: `http` vs `https` vs `http2`

## 1. `http` Module — _Classic Web Server_
- **Purpose**: To create basic HTTP/1.1 servers and handle web requests.
- **Use case**: Great for building simple servers, APIs, or learning how HTTP works under the hood.
- **Example**: Serving HTML or JSON over http://localhost:3000

---

## 2. `https` Module — _Secure Web Server_
- **Purpose**: Just like http, but adds **SSL/TLS encryption** (i.e., secure https:// connections).
- **Use case**: When you need secure communication — e.g., user logins, payments, or any production web service.
- **Setup**: Requires an SSL certificate (can be self-signed or from services like Let’s Encrypt).

---

## 3. `http2` Module — _Faster, Smarter Web Server_
- **Purpose**: To build servers using **HTTP/2**, a more modern, efficient protocol.
- **Key Features**:
  - **Multiplexing**: Multiple requests/responses over a single connection.
  - **Header Compression**: Reduces overhead.
  - **Server Push**: Proactively sends resources to the client.
- **Use case**: High-performance web apps, real-time systems, or when optimizing for speed and scalability.
- **Secure by default** (TLS required for browsers).

---

## HTTP/1.1 vs HTTP/2 — Key Differences

| Feature               | HTTP/1.1                    | HTTP/2                                 |
|-----------------------|-----------------------------|----------------------------------------|
| Connection Handling   | One request per connection  | Multiplexed (many streams per socket)  |
| Headers               | Sent in full every time     | Compressed using HPACK                 |
| Server Push           | Not supported               | Built-in                               |
| Speed & Performance   | Slower under load           | Much faster, especially with many small requests |

---

## When to Use Each

| Module   | When to Use                                                    |
|----------|----------------------------------------------------------------|
| http     | Prototypes, simple tools, internal APIs without sensitive data |
| https    | Any app in production, especially with users or sensitive data |
| http2    | Performance-critical apps (e.g., SPAs, streaming, real-time)   |


