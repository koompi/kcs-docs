<h1>Admins Page</h1>

<details close="close">
<summary><b>POST</b> /private/api/admin/add</summary>

 ---

 |      Header      |                 Data Type               |
 | ---------------- | --------------------------------------- |
 |  Authorization   |                 `String`                |

 |     Variable     |                 Data Type               |
 | ---------------- | --------------------------------------- |
 |   display_name   |                 `String`                |
 |     username     |       No UTF8, No Space `String`        |
 |     password     |                 `String`                |
 |       role       |      `Admin` or `Root` as `String`      |
 
 Body
 ```json
 {
    "display_name" : "Isaac Jackson Reay",
    "username": "isaac",
    "password": "123",
    "role": "Admin"
 }
 ```

 Response 200 
 ```
 ```

 |     Error    |             Body           |
 | ------------ | -------------------------- |
 |     401      |             Gone           |
 |     401      |          Unauthorized      |
 |     500      |   actual_error_goes_here   |

 - Note: 
   - `Authorization` Header value is `Bearer`
   - Only role `root` can perform this API. Anything else is 410 or 401
   - Only `exp` valid JWT will be allowed to use this API. Anything else is 410 or 401

 ---
</details>

<details close="close">
<summary><b>PUT</b> /private/api/admin/edit/{user_id}</summary>

 ---

 |      Header      |                 Data Type               |
 | ---------------- | --------------------------------------- |
 |  Authorization   |                 `String`                |


 | Query Parameters |                                       Data Type                                          |
 | ---------------- | ---------------------------------------------------------------------------------------- |
 |     user_id      |                                         UUID                                             |

 |     Variable     |                 Data Type               |
 | ---------------- | --------------------------------------- |
 |   display_name   |                 `String`                |
 |     username     |       No UTF8, No Space `String`        |
 |     password     |                 `String`                |
 |       role       |      `Admin` or `Root` as `String`      |
 
 Body 1 (without changing password)
 ```json
 {
    "display_name" : "New Isaac Jackson Reay",
    "username": "isaac_new",
    "role": "root",
 }
 ```

 Body 2 (without changing role)
 ```json
 {
    "display_name" : "New Isaac Jackson Reay",
    "username": "isaac_new_new",
    "password": "new_password_123",
 }
 ```

  Body 3 (full)
 ```json
 {
    "display_name" : "New Isaac Jackson Reay",
    "username": "isaac",
    "password": "new_password_123",
    "role": "root"
 }
 ```


 Response 200 
 ```
 ```

 |     Error    |             Body           |
 | ------------ | -------------------------- |
 |     401      |             Gone           |
 |     401      |          Unauthorized      |
 |     500      |   actual_error_goes_here   |

 - Note: 
   - `Authorization` Header value is `Bearer`
   - `username` cannot be edited.
   - All arguments beside `username` is `optional` and can be left out if unused
   - Only role `root` can perform this API. Anything else is 410 or 401
   - Only `exp` valid JWT will be allowed to use this API. Anything else is 410 or 401
   - example of UUID: `"76b4ff27-c39e-4ac8-b161-708f487b3f64"`

 ---
</details>

<details close="close">
<summary><b>DELETE</b> /private/api/admin/delete/{user_id}</summary>

 ---

 |      Header      |                 Data Type               |
 | ---------------- | --------------------------------------- |
 |  Authorization   |                 `String`                |

 | Query Parameters |                                       Data Type                                          |
 | ---------------- | ---------------------------------------------------------------------------------------- |
 |     user_id      |                                         UUID                                             |
 
 Body
 ```json
 ```

 Response 200 
 ```
 ```

 |     Error    |             Body           |
 | ------------ | -------------------------- |
 |     401      |             Gone           |
 |     401      |          Unauthorized      |
 |     500      |   actual_error_goes_here   |

 - Note: 
   - `Authorization` Header value is `Bearer`
   - Only role `root` can perform this API. Anything else is 410 or 401
   - Only `exp` valid JWT will be allowed to use this API. Anything else is 410 or 401
   - example of UUID: `"76b4ff27-c39e-4ac8-b161-708f487b3f64"`

 ---
</details>

<details close="close">
<summary><b>GET</b> /private/api/admin/query</summary>

 ---

 |      Header      |                 Data Type               |
 | ---------------- | --------------------------------------- |
 |  Authorization   |                 `String`                |

 |     Variable     |                 Data Type               |
 | ---------------- | --------------------------------------- |
 |       None       |                   None                  |
 
 Body
 ```json
 ```

 Response 200 
 ```json
 [
  {
    "user_id": "8d225eb4-b6a2-4f7d-bfcf-39b833bfb840",
    "display_name": "Root",
    "username": "root",
    "password": null,
    "role": "Root"
  },
  {
    "user_id": "92ee20e3-cb98-479d-9204-c5b4a472b2db",
    "display_name": "Isaac",
    "username": "isaac",
    "password": null,
    "role": "Admin"
  }
]
 ```

 |     Error    |             Body           |
 | ------------ | -------------------------- |
 |     401      |             Gone           |
 |     401      |          Unauthorized      |
 |     500      |   actual_error_goes_here   |

 - Note: 
   - `Authorization` Header value is `Bearer`
   - Only role `root` can perform this API. Anything else is 410 or 401
   - Only `exp` valid JWT will be allowed to use this API. Anything else is 410 or 401

 ---
</details>

<details close="close">
<summary><b>GET</b> /private/api/admin/query/{user_id}</summary>

 ---

 |      Header      |                 Data Type               |
 | ---------------- | --------------------------------------- |
 |  Authorization   |                 `String`                |

 | Query Parameters |                                       Data Type                                          |
 | ---------------- | ---------------------------------------------------------------------------------------- |
 |     user_id      |                                         UUID                                             |
 
 Body
 ```json
 ```

 Response 200 
 ```json
  {
    "user_id": "8d225eb4-b6a2-4f7d-bfcf-39b833bfb840",
    "display_name": "Root",
    "username": "root",
    "password": null,
    "role": "Root"
  }
 ```

 |     Error    |             Body           |
 | ------------ | -------------------------- |
 |     401      |             Gone           |
 |     401      |          Unauthorized      |
 |     500      |   actual_error_goes_here   |

 - Note: 
   - `Authorization` Header value is `Bearer`
   - Only role `root` can perform this API. Anything else is 410 or 401
   - Only `exp` valid JWT will be allowed to use this API. Anything else is 410 or 401
   - example of UUID: `"76b4ff27-c39e-4ac8-b161-708f487b3f64"`

 ---
</details>