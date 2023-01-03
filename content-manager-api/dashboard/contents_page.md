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
<summary><b>DELETE</b> /private/api/delete/{file_id}</summary>

 ---

 |      Header      |                 Data Type               |
 | ---------------- | --------------------------------------- |
 |  Authorization   |                 `String`                |


 | Query Parameters |                                       Data Type                                          |
 | ---------------- | ---------------------------------------------------------------------------------------- |
 |     file_id      |                                         UUID                                             |

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
   - Only `exp` valid JWT will be allowed to use this API. Anything else is 410 or 401
   - example of UUID: `"76b4ff27-c39e-4ac8-b161-708f487b3f64"`

 ---
</details>

<details close="close">
<summary><b>DELETE</b> /private/api/delete/{grade}/{subject}/{file_id}</summary>

 ---

 |      Header      |                 Data Type               |
 | ---------------- | --------------------------------------- |
 |  Authorization   |                 `String`                |


 | Query Parameters |                                       Data Type                                          |
 | ---------------- | ---------------------------------------------------------------------------------------- |
 |      grade       |                                    1, 2, 3, 4, 5, 6                                      |
 |     subjects     | Art, BasicPL, English, French, ICT, MindMotion, PE, PreMath, PreWriting, Science, Social |
 |     file_id      |                                         UUID                                             |

 | Query Parameters |                                       Data Type                                          |
 | ---------------- | ---------------------------------------------------------------------------------------- |
 |       None       |                                         None                                             | 

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
   - Only `exp` valid JWT will be allowed to use this API. Anything else is 410 or 401
   - example of UUID: `"76b4ff27-c39e-4ac8-b161-708f487b3f64"`

 ---
</details>

<details close="close">
<summary><b>GET</b> /public/api/query/pagination?</summary>

 ---

 |      Header      |                 Data Type               |
 | ---------------- | --------------------------------------- |
 |      None        |                   None                  |

 |   Query String   |                       Data Type                            |
 | ---------------- | ---------------------------------------------------------- |
 |   result_limit   |        `Unsigned Integer 32 Bit` in `Row` eg. 1000         |
 |    page_number   |          `Unsigned Integer 32 Bit` in `page` eg. 3         |
 
 Eg. ``http://unicefbackend.koompi.app/public/api/query/pagination?result_limit=2&page_number=3``
 
 Body
 ```
 ```

 Response 200 
 ```json
 {
   "page_count": 3,
   "current_page_number": 3,
   "data": [
     {
       "file_id": "1e433a7a-c13d-4752-bcab-79ee25af9088",
       "display_name": "p044រឿងកង្កែបធំ",
       "filename": "00000000-0000-0000-0000-0184a9b5987ccDA0NOGemuGev+GehOGegOGehOGfkuGegOGfguGelOGekuGfhg--.pdf",
       "location": "contents/FolkLore/ProvLang",
       "grade": "FolkLore",
       "subject": "ProvLang",
       "file_type": "PDF",
       "thumbnail": {
         "thumbnail_name": "00000000-0000-0000-0000-0184a9b5988bcDA0NOGemuGev+GehOGegOGehOGfkuGegOGfguGelOGekuGfhi10aHVtYm5haWw-.webp",
         "thumbnail_location": "contents/FolkLore/ProvLang"
       },
       "grade_kh": "សៀវភៅរឿងនិទាន",
       "subject_kh": "ភាសាព្រៅ"
     },
     {
      "file_id": "cc7911f3-1497-4f27-b7c1-a9bf7d3b031d",
       "display_name": "p072ប្រាជ្ញាថាវកង្កែប",
       "filename": "00000000-0000-0000-0000-0184a9b5ec94cDA3MuGelOGfkuGemuGetuGeh+GfkuGeieGetuGekOGetuGenOGegOGehOGfkuGegOGfguGelA--.pdf",
       "location": "contents/FolkLore/ProvLang",
       "grade": "FolkLore",
       "subject": "ProvLang",
       "file_type": "PDF",
       "thumbnail": {
         "thumbnail_name": "00000000-0000-0000-0000-0184a9b5ec9fcDA3MuGelOGfkuGemuGetuGeh+GfkuGeieGetuGekOGetuGenOGegOGehOGfkuGegOGfguGelC10aHVtYm5haWw-.webp",
         "thumbnail_location": "contents/FolkLore/ProvLang"
       },
       "grade_kh": "សៀវភៅរឿងនិទាន",
       "subject_kh": "ភាសាព្រៅ"
     }
   ]
 }
 ```
 
 |     Error    |             Body           |
 | ------------ | -------------------------- |
 |     500      |   actual_error_goes_here   |

 - Note: 
   - for `<a>` tag, property `src=` use `location + / + filename`
   - thumbnail `dimension` is `up to frontend settings` and `use with care on frontend`

 ---
</details>

---

<h2>To Be Deprecated</h2>

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