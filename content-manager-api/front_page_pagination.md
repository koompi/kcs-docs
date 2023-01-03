<h1>Front Page</h1>

<details close="close">
<summary><b>GET</b> /public/api/query/{grade}/{subject}/{file_id}</summary>

 ---

 |      Header      |                 Data Type               |
 | ---------------- | --------------------------------------- |
 |      None        |                   None                  |

 | Query Parameters |                                        Data Type                                         |
 | ---------------- | ---------------------------------------------------------------------------------------- |
 |      grade       |                                     1, 2, 3, 4, 5, 6                                     |
 |     subjects     | Art, BasicPL, English, French, ICT, MindMotion, PE, PreMath, PreWriting, Science, Social |
 
 Body
 ```
 ```

 Response 200 
 ```json
  {
    "file_id": "76b4ff27-c39e-4ac8-b161-708f487b3f64",
    "display_name": "លិខិតផ្ទេរសិទ្ធិ KOOMPI-MakaraV",
    "filename": "00000000-0000-0000-0000-01843d52e58b4Z6b4Z634Z6B4Z634Z6P4Z6V4Z+S4Z6R4Z+B4Z6a4Z6f4Z634Z6R4Z+S4Z6S4Z63IEtPT01QSS1NYWthcmFW.pdf",
    "location": "contents/Grade1/PE",
    "grade": "Grade1",
    "subject": "PE",
    "file_type": "PDF",
    "thumbnail": {
      "thumbnail_name": "00000000-0000-0000-0000-01843d52e58edGg=.png",
      "thumbnail_location": "contents/Grade1/PE"
    },
    "grade_kh": "ថ្នាក់ទី១",
    "subject_kh": "អប់រំកាយនិងកីឡា"
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

<details close="close">
<summary><b>GET</b> /public/api/query/{grade}/{subject}/pagination?</summary>

 ---

 |      Header      |                 Data Type               |
 | ---------------- | --------------------------------------- |
 |      None        |                   None                  |

 | Query Parameters |                                       Data Type                                          |
 | ---------------- | ---------------------------------------------------------------------------------------- |
 |      grade       |                                     1, 2, 3, 4, 5, 6                                     |
 |     subjects     | Art, BasicPL, English, French, ICT, MindMotion, PE, PreMath, PreWriting, Science, Social |

 |   Query String   |                       Data Type                            |
 | ---------------- | ---------------------------------------------------------- |
 |   result_limit   |        `Unsigned Integer 32 Bit` in `Row` eg. 1000         |
 |    page_number   |          `Unsigned Integer 32 Bit` in `page` eg. 3         |
 
 Eg. ``http://unicefbackend.koompi.app//public/api/query/Grade1/KhmerLang/pagination?result_limit=2&page_number=3``

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

<details close="close">
<summary><b>GET</b> /public/api/query/{grade}/pagination?</summary>

 ---

 |      Header      |                 Data Type               |
 | ---------------- | --------------------------------------- |
 |      None        |                   None                  |

 | Query Parameters |                                       Data Type                                          |
 | ---------------- | ---------------------------------------------------------------------------------------- |
 |      grade       |                                    1, 2, 3, 4, 5, 6                                      |
 
 |   Query String   |                       Data Type                            |
 | ---------------- | ---------------------------------------------------------- |
 |   result_limit   |        `Unsigned Integer 32 Bit` in `Row` eg. 1000         |
 |    page_number   |          `Unsigned Integer 32 Bit` in `page` eg. 3         |
 
 Eg. ``http://unicefbackend.koompi.app//public/api/query/Grade1/pagination?result_limit=2&page_number=3``

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
 
 Eg. ``http://unicefbackend.koompi.app//public/api/query/pagination?result_limit=2&page_number=3``
 
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

<details close="close">
<summary><b>GET</b> /public/api/search?</summary>

 ---

 |      Header      |                 Data Type               |
 | ---------------- | --------------------------------------- |
 |      None        |                   None                  |

 |   Query String   |                       Data Type                            |
 | ---------------- | ---------------------------------------------------------- |
 |  search_string   |                  `String` eg. ឯកសារ.pdf                    |
 |   result_limit   |        `Unsigned Integer 32 Bit` in `Row` eg. 1000         |
 |    page_number   |          `Unsigned Integer 32 Bit` in `page` eg. 3         |

 Eg. ``http://unicefbackend.koompi.app/public/api/search?search_string=កង្កែប&result_limit=2&page_number=3``
 
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

<details close="close">
<summary><b>GET</b> /public/api/sidebar</summary>

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
     "category_id": "Grade1",
     "category_display_name": "ថ្នាក់ទី1",
     "subcategory": [
       {
         "subcategory_id": "MindMotion",
         "subcategory_display_name": "ចិត្តចលភាព"
       },
       {
         "subcategory_id": "PreMath",
         "subcategory_display_name": "បុរេគណិត"
       }
     ]
   },
   {
     "category_id": "Grade6",
     "category_display_name": "ថ្នាក់ទី6",
     "subcategory": [
       {
         "subcategory_id": "MindMotion",
         "subcategory_display_name": "ចិត្តចលភាព"
       },
       {
         "subcategory_id": "PreMath",
         "subcategory_display_name": "បុរេគណិត"
       }
     ]
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