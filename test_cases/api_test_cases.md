# REST API — Test Cases

**Application:** ReqRes Public API (https://reqres.in)  
**Prepared by:** Mohammed Saqib  
**Date:** May 2026  
**Total Test Cases:** 15

---

## GET /api/users — Retrieve User List

### TC001 — Get users list page 1

| Field | Detail |
|---|---|
| Method | GET |
| Endpoint | /api/users?page=1 |
| Priority | High |
| Type | Positive |

**Expected:** Status 200, JSON with `data` array, `page=1`  
**Status:** *(Pass/Fail)*

---

### TC002 — Get users with invalid page number

| Field | Detail |
|---|---|
| Method | GET |
| Endpoint | /api/users?page=9999 |
| Priority | Medium |
| Type | Negative |

**Expected:** Status 200 with empty `data` array OR status 404  
**Status:** *(Pass/Fail)*

---

### TC003 — Get single user that exists

| Field | Detail |
|---|---|
| Method | GET |
| Endpoint | /api/users/2 |
| Priority | High |
| Type | Positive |

**Expected:** Status 200, user object with `id`, `email`, `first_name`, `last_name`, `avatar`  
**Status:** *(Pass/Fail)*

---

### TC004 — Get single user that does not exist

| Field | Detail |
|---|---|
| Method | GET |
| Endpoint | /api/users/9999 |
| Priority | High |
| Type | Negative |

**Expected:** Status 404, empty body or error message  
**Status:** *(Pass/Fail)*

---

## POST /api/users — Create User

### TC005 — Create user with valid payload

| Field | Detail |
|---|---|
| Method | POST |
| Endpoint | /api/users |
| Priority | High |
| Type | Positive |
| Body | `{"name": "Mohammed Saqib", "job": "QA Engineer"}` |

**Expected:** Status 201, response includes `id` and `createdAt`  
**Status:** *(Pass/Fail)*

---

### TC006 — Create user with empty name

| Field | Detail |
|---|---|
| Method | POST |
| Endpoint | /api/users |
| Priority | Medium |
| Type | Negative |
| Body | `{"name": "", "job": "QA Engineer"}` |

**Expected:** Status 400, validation error  
**Status:** *(Pass/Fail)*

---

### TC007 — Create user with missing required field

| Field | Detail |
|---|---|
| Method | POST |
| Endpoint | /api/users |
| Priority | Medium |
| Type | Negative |
| Body | `{"job": "QA Engineer"}` (no name) |

**Expected:** Status 400, error indicating missing field  
**Status:** *(Pass/Fail)*

---

## POST /api/register — Registration

### TC008 — Register with valid credentials

| Field | Detail |
|---|---|
| Method | POST |
| Endpoint | /api/register |
| Priority | High |
| Type | Positive |
| Body | `{"email": "eve.holt@reqres.in", "password": "pistol"}` |

**Expected:** Status 200, response has `token` and `id`  
**Status:** *(Pass/Fail)*

---

### TC009 — Register with missing password

| Field | Detail |
|---|---|
| Method | POST |
| Endpoint | /api/register |
| Priority | High |
| Type | Negative |
| Body | `{"email": "sydney@fife"}` |

**Expected:** Status 400, `{"error": "Missing password"}`  
**Status:** *(Pass/Fail)*

---

### TC010 — Response time within acceptable limit

| Field | Detail |
|---|---|
| Method | GET |
| Endpoint | /api/users/1 |
| Priority | Medium |
| Type | Performance |

**Expected:** Response received within 3 seconds  
**Status:** *(Pass/Fail)*
