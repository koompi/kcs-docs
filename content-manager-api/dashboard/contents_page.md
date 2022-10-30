<h1>Contents Page</h1>

<details close="close">
<summary><b>POST</b> /private/api/upload/{grade}/{subject}/{type}</summary>

 ---

 |      Header      |                 Data Type               |
 | ---------------- | --------------------------------------- |
 |  Authorization   |                 `String`                |

 | Query Parameters |                                       Data Type                                          |
 | ---------------- | ---------------------------------------------------------------------------------------- |
 |      grade       |                                    1, 2, 3, 4, 5, 6                                      |
 |     subjects     | Art, BasicPL, English, French, ICT, MindMotion, PE, PreMath, PreWriting, Science, Social |
 |       type       |                                   PDF, Video, Audio                                      |


 
 Body

 |    Field Name    |                   Value                 |
 | ---------------- | --------------------------------------- |
 |       file       |   `required` `file` pdf, mp3, mp4...    |
 |    thumbnail     |   `optional` `file` png, jpg, bmp...    |


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
   - Only `exp` valid JWT will be allowed to use this API. Anything else is 410 or 401
   - Only valid Query Parameter will be allowed. Anything else is 500 with description 

 ---
</details>

<details close="close">
<summary><b>DELETE</b> /private/api/delete</summary>

 ---

 |      Header      |                 Data Type               |
 | ---------------- | --------------------------------------- |
 |  Authorization   |                 `String`                |

 | Query Parameters |                                       Data Type                                          |
 | ---------------- | ---------------------------------------------------------------------------------------- |
 |       None       |                                         None                                             | 

 Body (filename)
```json
"442++Zb4S64+B44664++684+4ZZSYZ46SB664B6ZP=Z446Z48P4=Z8ZaZL4Z64DgZ+66Z8+J4PSZ=4Z6ZAZAZ4UbZ+Ba6Z4ZPZ4Z.pdf"
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
   - Only `exp` valid JWT will be allowed to use this API. Anything else is 410 or 401

 ---
</details>

<details close="close">
<summary><b>GET</b> /public/api/query</summary>

 ---

 |      Header      |                 Data Type               |
 | ---------------- | --------------------------------------- |
 |      None        |                   None                  |
 
 Body
 ```
 ```

 Response 200 
 ```json
 [
   {
     "display_name": "សេក្តីប្រកាសតម្លៃពេញអាយូ",
     "filename": "442++Zb4S64+B44664++684+4ZZSYZ46SB664B6ZP=Z446Z48P4=Z8ZaZL4Z64DgZ+66Z8+J4PSZ=4Z6ZAZAZ4UbZ+Ba6Z4ZPZ4Z.pdf",
     "location": "contents/Grade1/Art",
     "grade": "Grade1",
     "subject": "Art",
     "file_type": "PDF",
     "thumbnail": {
       "thumbnail_name": "lLBYBuBBB1d1GW===WlnWWZY1l=ZLbLuudW=ZYunnWuYldlb=L11JWBGd=wYbn=GLLLwJBlllb=dnW1uuJBdYJl1s=d1uBBGLs1u.png",
       "thumbnail_location": "contents/Grade1/Art"
     }
   },
   {
     "display_name": "សេក្តីប្រកាសតម្លៃអាយូ គ្មានអគ្គីសនី គ្មានWIFI",
     "filename": "444ee64O4ZfGZhGDA+64uba44AZh4YkGSZ4DZ+Lp4444DAZf6egSj4JZaa=A4GureeXo6n4GZ4PZ6gn+JZuAZe6++4f6ZC4b6Gku.pdf",
     "location": "contents/Grade1/Art",
     "grade": "Grade1",
     "subject": "Art",
     "file_type": "PDF",
     "thumbnail": {
       "thumbnail_name": "uhBnWnu=WGw1=sbYWssJ11=GWduWnnbZwhwdnl=wGwb==b=WGdJbZsGWlZuW1dubuhlJJ=WllBhwLB=sl=hsW1lu1lGGuL==LWWu.png",
       "thumbnail_location": "contents/Grade1/Art"
     }
   }
 ]
 ```
 
 |     Error    |             Body           |
 | ------------ | -------------------------- |
 |     500      |   actual_error_goes_here   |

 - Note: 
   - for `<a>` tag, property `src=` use `location + / + filename`
   - thumbnail `dimension` is `up to frontend settings` and `use with care on frontend`

 ---
</details>