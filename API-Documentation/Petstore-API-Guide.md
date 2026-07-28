# Petstore API Guide

| Version | 1.0 |
|----------|-----|
| Last Updated | July 2026 |
| Author | Shilpa Sreedhar P |

---

# Overview

The Petstore API is a RESTful web service that enables applications to manage pet information. The API supports operations such as creating, retrieving, updating, and deleting pet records.

This guide describes the authentication method, request format, response format, and commonly used API endpoints.

---

# Base URL

```
https://petstore3.swagger.io/api/v3
```

---

# Authentication

The Petstore API supports API key authentication.

Include the API key in the request header.

| Header | Value |
|---------|-------|
| api_key | Your API Key |

---

# Response Format

All API responses are returned in JSON format.

---

# HTTP Methods

| Method | Description |
|---------|-------------|
| GET | Retrieve data |
| POST | Create a resource |
| PUT | Update a resource |
| DELETE | Delete a resource |
