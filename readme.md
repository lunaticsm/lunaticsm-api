<p align="center">
    <img src="https://lunaticsm.web.id" alt="Lunaticsm Logo" width="150"/>
    <br>
    <b style="font-size: 32px;">Lunaticsm API</b>
    <br>
    <a href="https://lunaticsm.web.id/">Homepage</a>
    •
    <a href="https://github.com/lunaticsm/lunaticsm-api/releases">Releases</a>
    •
    <a href="https://t.me/lunaticsmchat">Support</a>
</p>

# 🚀 Lunaticsm API

> **Lunaticsm API** is a robust and secure file upload and sharing service designed to seamlessly integrate with your applications. Whether you're a developer looking to automate file uploads or manage files programmatically, Lunaticsm API provides all the tools you need.

## 📑 Table of Contents

- [✨ Features](#-features)
- [🔧 Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
- [🔐 Authentication](#-authentication)
- [🛠️ API Endpoints](#️-api-endpoints)
  - [1. File Upload](#1-file-upload)
    - [🔓 Guest Upload](#-guest-upload)
    - [🔑 Authenticated Upload](#-authenticated-upload)
    - [🌐 Upload via URL](#-upload-via-url)
  - [2. File Deletion](#2-file-deletion)
- [⚠️ Error Handling](#️-error-handling)
- [⏱️ Rate Limiting](#️-rate-limiting)
- [💻 Examples](#-examples)
  - [Using Python](#using-python)
  - [Using JavaScript (Fetch API)](#using-javascript-fetch-api)
- [🔗 Third-Party Integrations](#-third-party-integrations)
- [📞 Support](#-support)
- [📜 License](#-license)

## ✨ Features

- **Secure File Upload:** Upload files directly or via URL with robust security measures.
- **Guest and Authenticated Access:** Support for both unregistered users and registered users with enhanced capabilities.
- **API Key Management:** Easily generate and revoke API keys for secure access.
- **Comprehensive File Management:** Upload, list, and delete files effortlessly through the API.
- **Rate Limiting:** Ensure fair usage and protect against abuse with configurable rate limits.
- **Seamless Integrations:** Compatible with popular tools like ShareX and Rclone for extended functionality.

## 🔧 Getting Started

### Prerequisites

- **HTTP Client:** Tools like `curl`, Postman, or any programming language with HTTP capabilities.
- **API Key:** Required for authenticated requests.


## 🔐 Authentication

Lunaticsm API uses **API Keys** for authentication. To perform authenticated requests, include your API Key in the `Authorization` header using the `Bearer` scheme.

### Example Header

```http
Authorization: Bearer YOUR_API_KEY
```

## 🛠️ API Endpoints

### 1. File Upload

#### 🔓 Guest Upload
- **Endpoint:** `/upload/`
- **Method:** `POST`
- **Headers:** 
    - `Content-Type: multipart/form-data`

```bash
curl -F "files=@/path/to/file.png" https://lunaticsm.web.id/upload/
```

#### 🔑 Authenticated Upload
- **Endpoint:** `/upload/`
- **Method:** `POST`
- **Headers:** 
    - `Authorization: Bearer YOUR_API_KEY`
    - `Content-Type: multipart/form-data`

```bash
curl -H "Authorization: Bearer YOUR_API_KEY" -F "files=@/path/to/file.png" https://lunaticsm.web.id/upload/
```

#### 🌐 Upload via URL
- **Endpoint:** `/upload/url/`
- **Method:** `POST`
- **Body:** `file_url` (string)

```bash
curl -X POST -d "file_url=https://example.com/image.jpg" https://lunaticsm.web.id/upload/url/
```

---

### 2. File Deletion
- **Endpoint:** `/delete/{short_code}/`
- **Method:** `POST`

```bash
curl -H "Authorization: Bearer YOUR_API_KEY" -X POST https://lunaticsm.web.id/delete/SHORT_CODE
```

---


## ⚠️ Error Handling

- `200 OK`: The request was successful.
- `400 Bad Request`: The request was invalid.
- `401 Unauthorized`: Authentication failed.
- `403 Forbidden`: User does not have access.
- `404 Not Found`: Resource not found.
- `429 Too Many Requests`: Rate limit exceeded.
- `500 Internal Server Error`: Server error.
=
## 📞 Support

If you encounter any issues or have questions regarding the Lunaticsm API, feel free to reach out:

- **Email:** support@lunaticsm.web.id
- **Telegram:** [t.me/LunaticsmSupport](https://t.me/lunaticsmchat)

## 📜 License

Distributed under the MIT License. See `LICENSE` for more information.

---

© 2025 Lunaticsm | Privacy | Terms of Service | DMCA | FAQ | API Documentation
