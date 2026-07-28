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

# Get Pet by ID

Retrieves the details of a specific pet.

## Endpoint

GET /pet/{petId}

## Path Parameter

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| petId | Integer | Yes | Unique identifier of the pet |

## Example Request

GET /pet/101

## Success Response

Status Code: 200 OK

## Example Response

```json
{
  "id": 101,
  "name": "Buddy",
  "status": "available"
}
```
# Update a Pet

Updates an existing pet.

## Endpoint

PUT /pet

## Request Body

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| id | Integer | Yes | Pet ID |
| name | String | Yes | Pet name |
| status | String | Yes | Current status |

## Example Request

```json
{
  "id": 101,
  "name": "Buddy",
  "status": "sold"
}
```

## Success Response

Status Code: 200 OK

# Delete a Pet

Deletes an existing pet.

## Endpoint

DELETE /pet/{petId}

## Path Parameter

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| petId | Integer | Yes | Pet ID |

## Example Request

DELETE /pet/101

## Success Response

Status Code: 200 OK

# Error Codes

| Status Code | Description |
|------------|-------------|
| 200 | Request completed successfully |
| 400 | Invalid request |
| 401 | Unauthorized |
| 404 | Resource not found |
| 500 | Internal server error |

# Best Practices

- Validate request parameters before sending the request.
- Use HTTPS for all API requests.
- Handle HTTP status codes appropriately.
- Store API keys securely.
- Review API responses before processing the returned data.
