<h1>Front Page</h1>

<details close="close">
<summary><b>GET</b> /public/api/query/{grade}/{subject}</summary>

 ---

 |      Header      |                 Data Type               |
 | ---------------- | --------------------------------------- |
 |      None        |                   None                  |

 | Query Parameters |                                       Data Type                                          |
 | ---------------- | ---------------------------------------------------------------------------------------- |
 |      grade       |                                     1, 2, 3, 4, 5, 6                                     |
 |     subjects     | Art, BasicPL, English, French, ICT, MindMotion, PE, PreMath, PreWriting, Science, Social |
 
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

<details close="close">
<summary><b>GET</b> /public/api/query/{grade}</summary>

 ---

 |      Header      |                 Data Type               |
 | ---------------- | --------------------------------------- |
 |      None        |                   None                  |

 | Query Parameters |                                       Data Type                                          |
 | ---------------- | ---------------------------------------------------------------------------------------- |
 |      grade       |                                    1, 2, 3, 4, 5, 6                                      |
 
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
      },
      {
        "subcategory_id": "PreWriting",
        "subcategory_display_name": "បុរេសំណេរ"
      },
      {
        "subcategory_id": "Art",
        "subcategory_display_name": "អប់រំសិល្បៈ"
      },
      {
        "subcategory_id": "PE",
        "subcategory_display_name": "អប់រំកាយនិងកីឡា"
      }
    ]
  },
  {
    "category_id": "Grade2",
    "category_display_name": "ថ្នាក់ទី2",
    "subcategory": [
      {
        "subcategory_id": "MindMotion",
        "subcategory_display_name": "ចិត្តចលភាព"
      },
      {
        "subcategory_id": "PreMath",
        "subcategory_display_name": "បុរេគណិត"
      },
      {
        "subcategory_id": "PreWriting",
        "subcategory_display_name": "បុរេសំណេរ"
      },
      {
        "subcategory_id": "Art",
        "subcategory_display_name": "អប់រំសិល្បៈ"
      },
      {
        "subcategory_id": "PE",
        "subcategory_display_name": "អប់រំកាយនិងកីឡា"
      }
    ]
  },
  {
    "category_id": "Grade3",
    "category_display_name": "ថ្នាក់ទី3",
    "subcategory": [
      {
        "subcategory_id": "MindMotion",
        "subcategory_display_name": "ចិត្តចលភាព"
      },
      {
        "subcategory_id": "PreMath",
        "subcategory_display_name": "បុរេគណិត"
      },
      {
        "subcategory_id": "PreWriting",
        "subcategory_display_name": "បុរេសំណេរ"
      },
      {
        "subcategory_id": "Art",
        "subcategory_display_name": "អប់រំសិល្បៈ"
      },
      {
        "subcategory_id": "PE",
        "subcategory_display_name": "អប់រំកាយនិងកីឡា"
      }
    ]
  },
  {
    "category_id": "Grade4",
    "category_display_name": "ថ្នាក់ទី4",
    "subcategory": [
      {
        "subcategory_id": "MindMotion",
        "subcategory_display_name": "ចិត្តចលភាព"
      },
      {
        "subcategory_id": "PreMath",
        "subcategory_display_name": "បុរេគណិត"
      },
      {
        "subcategory_id": "PreWriting",
        "subcategory_display_name": "បុរេសំណេរ"
      },
      {
        "subcategory_id": "Science",
        "subcategory_display_name": "វិទ្យាសាស្រ្ត"
      },
      {
        "subcategory_id": "Social",
        "subcategory_display_name": "សង្គម"
      },
      {
        "subcategory_id": "Art",
        "subcategory_display_name": "អប់រំសិល្បៈ"
      },
      {
        "subcategory_id": "PE",
        "subcategory_display_name": "អប់រំកាយនិងកីឡា"
      },
      {
        "subcategory_id": "French",
        "subcategory_display_name": "ភាសាបារាំង"
      },
      {
        "subcategory_id": "English",
        "subcategory_display_name": "ភាសាអង់គ្លេស"
      },
      {
        "subcategory_id": "ICT",
        "subcategory_display_name": "ព័ត៌មានវិទ្យា"
      },
      {
        "subcategory_id": "BasicPL",
        "subcategory_display_name": "បំណិនជីវិតមូលដ្ឋាន"
      }
    ]
  },
  {
    "category_id": "Grade5",
    "category_display_name": "ថ្នាក់ទី5",
    "subcategory": [
      {
        "subcategory_id": "MindMotion",
        "subcategory_display_name": "ចិត្តចលភាព"
      },
      {
        "subcategory_id": "PreMath",
        "subcategory_display_name": "បុរេគណិត"
      },
      {
        "subcategory_id": "PreWriting",
        "subcategory_display_name": "បុរេសំណេរ"
      },
      {
        "subcategory_id": "Science",
        "subcategory_display_name": "វិទ្យាសាស្រ្ត"
      },
      {
        "subcategory_id": "Social",
        "subcategory_display_name": "សង្គម"
      },
      {
        "subcategory_id": "Art",
        "subcategory_display_name": "អប់រំសិល្បៈ"
      },
      {
        "subcategory_id": "PE",
        "subcategory_display_name": "អប់រំកាយនិងកីឡា"
      },
      {
        "subcategory_id": "French",
        "subcategory_display_name": "ភាសាបារាំង"
      },
      {
        "subcategory_id": "English",
        "subcategory_display_name": "ភាសាអង់គ្លេស"
      },
      {
        "subcategory_id": "ICT",
        "subcategory_display_name": "ព័ត៌មានវិទ្យា"
      },
      {
        "subcategory_id": "BasicPL",
        "subcategory_display_name": "បំណិនជីវិតមូលដ្ឋាន"
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
      },
      {
        "subcategory_id": "PreWriting",
        "subcategory_display_name": "បុរេសំណេរ"
      },
      {
        "subcategory_id": "Science",
        "subcategory_display_name": "វិទ្យាសាស្រ្ត"
      },
      {
        "subcategory_id": "Social",
        "subcategory_display_name": "សង្គម"
      },
      {
        "subcategory_id": "Art",
        "subcategory_display_name": "អប់រំសិល្បៈ"
      },
      {
        "subcategory_id": "PE",
        "subcategory_display_name": "អប់រំកាយនិងកីឡា"
      },
      {
        "subcategory_id": "French",
        "subcategory_display_name": "ភាសាបារាំង"
      },
      {
        "subcategory_id": "English",
        "subcategory_display_name": "ភាសាអង់គ្លេស"
      },
      {
        "subcategory_id": "ICT",
        "subcategory_display_name": "ព័ត៌មានវិទ្យា"
      },
      {
        "subcategory_id": "BasicPL",
        "subcategory_display_name": "បំណិនជីវិតមូលដ្ឋាន"
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