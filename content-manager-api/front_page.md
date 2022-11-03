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
<summary><b>GET</b> /public/api/query/{grade}/{subject}</summary>

 ---

 |      Header      |                 Data Type               |
 | ---------------- | --------------------------------------- |
 |      None        |                   None                  |

 | Query Parameters |        ~                               Data Type                                          |
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
  },
  {
    "file_id": "9e955ff6-362c-4af2-bfa3-e23e0c15c1a8",
    "display_name": "សេក្តីប្រកាសតម្លៃពេញអាយូ",
    "filename": "00000000-0000-0000-0000-01843d535e1e4Z6f4Z+B4Z6A4Z+S4Z6P4Z644Z6U4Z+S4Z6a4Z6A4Z624Z6f4Z6P4Z6Y4Z+S4Z6b4Z+D4Z6W4Z+B4Z6J4Z6i4Z624Z6Z4Z68.pdf",
    "location": "contents/Grade1/Art",
    "grade": "Grade1",
    "subject": "Art",
    "file_type": "PDF",
    "thumbnail": {
      "thumbnail_name": "00000000-0000-0000-0000-01843d535e1f4Z6f4Z+B4Z6A4Z+S4Z6P4Z644Z6U4Z+S4Z6a4Z6A4Z624Z6f4Z6P4Z6Y4Z+S4Z6b4Z+D4Z6W4Z+B4Z6J4Z6i4Z624Z6Z4Z68.pdf",
      "thumbnail_location": "contents/Grade1/Art"
    },
    "grade_kh": "ថ្នាក់ទី១",
    "subject_kh": "អប់រំសិល្បៈ"
  },
  {
    "file_id": "5c8b58bc-945b-4ec8-8ef2-73caab3f0e48",
    "display_name": "video_2022-11-03_18-53-00",
    "filename": "00000000-0000-0000-0000-01843d585ddedmlkZW9fMjAyMi0xMS0wM18xOC01My0wMA==.mp4",
    "location": "contents/Grade1/Science",
    "grade": "Grade1",
    "subject": "Science",
    "file_type": "Video",
    "thumbnail": {
      "thumbnail_name": "00000000-0000-0000-0000-01843d585df1cGhvdG9fMjAyMi0xMS0wM18xOC01NC0zMQ==.jpg",
      "thumbnail_location": "contents/Grade1/Science"
    },
    "grade_kh": "ថ្នាក់ទី១",
    "subject_kh": "វិទ្យាសាស្រ្ត"
  },
  {
    "file_id": "03434b1f-79f1-4f07-857f-8f39081b6668",
    "display_name": "7 Years",
    "filename": "00000000-0000-0000-0000-01843d58b7e6NyBZZWFycw==.mp3",
    "location": "contents/Grade1/English",
    "grade": "Grade1",
    "subject": "English",
    "file_type": "Audio",
    "thumbnail": {
      "thumbnail_name": "00000000-0000-0000-0000-01843d58b7fdNy1ZZWFycy1ieS1MdWthcy1HcmFoYW0=.jpg",
      "thumbnail_location": "contents/Grade1/English"
    },
    "grade_kh": "ថ្នាក់ទី១",
    "subject_kh": "ភាសាអង់គ្លេស"
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
  },
  {
    "file_id": "9e955ff6-362c-4af2-bfa3-e23e0c15c1a8",
    "display_name": "សេក្តីប្រកាសតម្លៃពេញអាយូ",
    "filename": "00000000-0000-0000-0000-01843d535e1e4Z6f4Z+B4Z6A4Z+S4Z6P4Z644Z6U4Z+S4Z6a4Z6A4Z624Z6f4Z6P4Z6Y4Z+S4Z6b4Z+D4Z6W4Z+B4Z6J4Z6i4Z624Z6Z4Z68.pdf",
    "location": "contents/Grade1/Art",
    "grade": "Grade1",
    "subject": "Art",
    "file_type": "PDF",
    "thumbnail": {
      "thumbnail_name": "00000000-0000-0000-0000-01843d535e1f4Z6f4Z+B4Z6A4Z+S4Z6P4Z644Z6U4Z+S4Z6a4Z6A4Z624Z6f4Z6P4Z6Y4Z+S4Z6b4Z+D4Z6W4Z+B4Z6J4Z6i4Z624Z6Z4Z68.pdf",
      "thumbnail_location": "contents/Grade1/Art"
    },
    "grade_kh": "ថ្នាក់ទី១",
    "subject_kh": "អប់រំសិល្បៈ"
  },
  {
    "file_id": "5c8b58bc-945b-4ec8-8ef2-73caab3f0e48",
    "display_name": "video_2022-11-03_18-53-00",
    "filename": "00000000-0000-0000-0000-01843d585ddedmlkZW9fMjAyMi0xMS0wM18xOC01My0wMA==.mp4",
    "location": "contents/Grade1/Science",
    "grade": "Grade1",
    "subject": "Science",
    "file_type": "Video",
    "thumbnail": {
      "thumbnail_name": "00000000-0000-0000-0000-01843d585df1cGhvdG9fMjAyMi0xMS0wM18xOC01NC0zMQ==.jpg",
      "thumbnail_location": "contents/Grade1/Science"
    },
    "grade_kh": "ថ្នាក់ទី១",
    "subject_kh": "វិទ្យាសាស្រ្ត"
  },
  {
    "file_id": "03434b1f-79f1-4f07-857f-8f39081b6668",
    "display_name": "7 Years",
    "filename": "00000000-0000-0000-0000-01843d58b7e6NyBZZWFycw==.mp3",
    "location": "contents/Grade1/English",
    "grade": "Grade1",
    "subject": "English",
    "file_type": "Audio",
    "thumbnail": {
      "thumbnail_name": "00000000-0000-0000-0000-01843d58b7fdNy1ZZWFycy1ieS1MdWthcy1HcmFoYW0=.jpg",
      "thumbnail_location": "contents/Grade1/English"
    },
    "grade_kh": "ថ្នាក់ទី១",
    "subject_kh": "ភាសាអង់គ្លេស"
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
  },
  {
    "file_id": "9e955ff6-362c-4af2-bfa3-e23e0c15c1a8",
    "display_name": "សេក្តីប្រកាសតម្លៃពេញអាយូ",
    "filename": "00000000-0000-0000-0000-01843d535e1e4Z6f4Z+B4Z6A4Z+S4Z6P4Z644Z6U4Z+S4Z6a4Z6A4Z624Z6f4Z6P4Z6Y4Z+S4Z6b4Z+D4Z6W4Z+B4Z6J4Z6i4Z624Z6Z4Z68.pdf",
    "location": "contents/Grade1/Art",
    "grade": "Grade1",
    "subject": "Art",
    "file_type": "PDF",
    "thumbnail": {
      "thumbnail_name": "00000000-0000-0000-0000-01843d535e1f4Z6f4Z+B4Z6A4Z+S4Z6P4Z644Z6U4Z+S4Z6a4Z6A4Z624Z6f4Z6P4Z6Y4Z+S4Z6b4Z+D4Z6W4Z+B4Z6J4Z6i4Z624Z6Z4Z68.pdf",
      "thumbnail_location": "contents/Grade1/Art"
    },
    "grade_kh": "ថ្នាក់ទី១",
    "subject_kh": "អប់រំសិល្បៈ"
  },
  {
    "file_id": "5c8b58bc-945b-4ec8-8ef2-73caab3f0e48",
    "display_name": "video_2022-11-03_18-53-00",
    "filename": "00000000-0000-0000-0000-01843d585ddedmlkZW9fMjAyMi0xMS0wM18xOC01My0wMA==.mp4",
    "location": "contents/Grade1/Science",
    "grade": "Grade1",
    "subject": "Science",
    "file_type": "Video",
    "thumbnail": {
      "thumbnail_name": "00000000-0000-0000-0000-01843d585df1cGhvdG9fMjAyMi0xMS0wM18xOC01NC0zMQ==.jpg",
      "thumbnail_location": "contents/Grade1/Science"
    },
    "grade_kh": "ថ្នាក់ទី១",
    "subject_kh": "វិទ្យាសាស្រ្ត"
  },
  {
    "file_id": "03434b1f-79f1-4f07-857f-8f39081b6668",
    "display_name": "7 Years",
    "filename": "00000000-0000-0000-0000-01843d58b7e6NyBZZWFycw==.mp3",
    "location": "contents/Grade1/English",
    "grade": "Grade1",
    "subject": "English",
    "file_type": "Audio",
    "thumbnail": {
      "thumbnail_name": "00000000-0000-0000-0000-01843d58b7fdNy1ZZWFycy1ieS1MdWthcy1HcmFoYW0=.jpg",
      "thumbnail_location": "contents/Grade1/English"
    },
    "grade_kh": "ថ្នាក់ទី១",
    "subject_kh": "ភាសាអង់គ្លេស"
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