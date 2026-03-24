# API Testing with Postman (JSONPlaceholder)

## Overview
This project demonstrates API testing using Postman with the JSONPlaceholder API.

## Base URL
https://jsonplaceholder.typicode.com

---

## Test Cases

### 1. Get Post By ID
**Request:**
GET /posts/1

**Validations:**
- Status code is 200
- Response is JSON
- ID is 1
- Title exists

---

### 2. Get All Posts
**Request:**
GET /posts

**Validations:**
- Status code is 200
- Response is an array
- Array is not empty

---

### 3. Get User By ID
**Request:**
GET /users/1

**Validations:**
- Status code is 200
- User ID is 1
- Name exists
- Email exists

---

### 4. Get Invalid Post ID
**Request:**
GET /posts/9999

**Validations:**
- Status code is 404
- Response handles invalid resource correctly

---

### 5. Create New Post
**Request:**
POST /posts

**Body:**
```json
{
  "title": "QA Test Post",
  "body": "This is a test created in Postman",
  "userId": 1
}
