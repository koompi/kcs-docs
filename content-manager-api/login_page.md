<h1>Login Page</h1>

<details close="close">
<summary><b>POST</b> /public/api/login</summary>

 ---

 |      Header      |                 Data Type               |
 | ---------------- | --------------------------------------- |
 |      None        |                   None                  |
 
 Body
 ```json
 {
    "username": "root",
    "password": "123"
 }
 ```

 Response 200 
 ```json
 "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJhdWQiOiJyb290Iiwicm9sZSI6IlJvb3QiLCJpYXQiOjE2NjcxMzg0NzcsImV4cCI6MTY2NzEzOTA3N30.LrkkZSsJxYKxSXq2x1Qs_LIqNAe70RQ-7ghiUCHzecI"
 ```
 
 |     Error    |             Body           |
 | ------------ | -------------------------- |
 |     500      |   actual_error_goes_here   |

 - Note: 
   - First run `username` and `password` is at as `ROOT_INITIAL_USERNAME` and `ROOT_INITIAL_USERNAME` at `settings.toml` in `project` root directory
   - Decryption Key for that JWT token is as `DECRYPT_KEY` at `settings.toml` in `project` root directory
   - Claim contains 
     - `aud` for username of user as `String`, 
     - `role` for role of user as `String`, 
     - `iat` for time it was created as `Unsigned Integer 128`, and
     - `exp` for time it expire as `Unsigned Integer 128`
   - `exp` for claim is set as `TOKEN_EXPIRATION_SEC` at `settings.toml` in `project` root directory
 ---
</details>