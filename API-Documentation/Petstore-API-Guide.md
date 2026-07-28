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
# Create a Pet

Creates a new pet record.

## Endpoint

```
POST /pet
```

## Request Body

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| id | Integer | Yes | Unique pet identifier |
| name | String | Yes | Pet name |
| category | Object | No | Pet category |
| status | String | Yes | available, pending, sold |

## Example Request

```json
{
  "id": 101,
  "name": "Buddy",
  "status": "available"
}
```

## Success Response

**Status Code**

```
200 OK
```

## Example Response

```json
{
  "id":101,
  "name":"Buddy",
  "status":"available"
}
```

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
