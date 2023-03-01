<h1>Public Storage Page</h1>

<details close="close">
<summary><b>GET</b> /private/api/settings/storage/status/non_priv</summary>

 ---

 |      Header      |                 Data Type               |
 | ---------------- | --------------------------------------- |
 |       None       |                                         |
 
 Body
 ```json
 ```

 Response 200 
 ```json
[
  {
    "drive_label":  "Local  Content  Storage",
    "drive_partuuid":  {
     "drive_partuuid":  "kmp"
    },
    "free_space":  "3.3T",
    "total_space":  "3.6T",
    "percentage":  4,
    "public": true
  },
  {
    "drive_label":  "Removeable  Device",
    "drive_partuuid":  {
       "drive_partuuid":  "7df645f6-2912-4f6f-bc80-6e823e75e8cb"
    },
    "free_space":  "3.7G",
    "total_space":  "3.9G",
    "percentage":  1,
    "public": true
  },
  {
    "drive_label":  "Removeable  Device",
    "drive_partuuid":  {
      "drive_partuuid":  "3EB7-DF9A"
    },
    "free_space":  "4.0G",
    "total_space":  "4.0G",
    "percentage":  1,
    "public": true
  }
 ]
 ```

 |     Error    |             Body           |
 | ------------ | -------------------------- |
 |     500      |  *actual_error_goes_here*  |

 ---
</details>

<details close="close">
<summary><b>GET</b> /private/api/settings/storage/device/status/non_priv/<em>{drive_partuuid}</em></summary>

 ---

 |      Header      |                 Data Type               |
 | ---------------- | --------------------------------------- |
 |       None       |                                         |
 
 Body
 ```json
 ```

 Response 200 
 ```json
 {
   "name": "Removeable Device",
   "meta": {
      "item_last_modify_date": "2021-11-25 06:00:43",
      "item_is_dir": true,
      "item_size": 32768
   },
   "children": [
      {
         "name": "231_1- Keynote Proficient Student's Book_2016 -192p_backup.pdf",
         "meta": {
            "item_last_modify_date": "2021-11-24 12:18:53",
            "item_is_dir": false,
            "item_size": 30881022
         },
         "children": []
      },
      {
         "name": "231_1- Keynote Proficient Student's Book_2016 -192p.pdf",
         "meta": {
            "item_last_modify_date": "2021-11-24 13:16:09",
            "item_is_dir": false,
            "item_size": 30921636
         },
         "children": []
      },
      {
         "name": "Pichponereay NGOR_E4.8_Reflection Paper_Do School Kills Creativity.docx",
         "meta": {
            "item_last_modify_date": "2021-11-20 16:54:18",
            "item_is_dir": false,
            "item_size": 2955518
         },
         "children": []
      }
   ]
 }
 ```

 |     Error    |             Body           |
 | ------------ | -------------------------- |
 |     500      |  *actual_error_goes_here*  |

 ---
</details>

<details close="close">
<summary><b>GET</b> /private/api/settings/storage/device/serve-file?</summary>

 ---

 |   Query String   |                   Data Type                                |
 | ---------------- | ---------------------------------------------------------- |
 |    item_name     |                  `String` eg. ឯកសារ.pdf                    |
 | parent_directory |                  `String` eg. rootdir/subdir               |
 |  drive_partuuid  |                  `String` eg. kmp                          |
 
 Example 
 `https://localhost:8080/private/api/settings/storage/device/serve-file?item_name={}&parent_directory={}&drive_partuuid={}`

 Body
 ```json
 ```

 Response 200 
 ```
 ```

 |     Error    |             Body           |
 | ------------ | -------------------------- |
 |     500      |  *actual_error_goes_here*  |

 ---
</details>

<details close="close">
<summary><b>GET</b> /private/api/settings/storage/device/list?</summary>

 ---

 |      Header      |                 Data Type               |
 | ---------------- | --------------------------------------- |
 |       None       |                   None                  |
 
 | Query Parameters |        Data Type            |
 | ---------------- | --------------------------- |
 |    item_name     | `String` eg. `directory_1`  |
 | parent_directory | `String` eg. `directory_0`  |
 |  drive_partuuid  |      `String` eg. `kmp`     |

 eg: `http://koompi.kh/private/api/settings/storage/device/list?item_name={}&parent_directory={}&drive_partuuid={}`

 Body
 ```json
 ```

 Response 200 
 ```json
 {
   "drive_partuuid": "kmp",
   "parent_directory": "",
   "photo_size": "1.72 MB",
   "photo_count": "21",
   "audio_size": "0 B",
   "audio_count": "0",
   "video_size": "240.71 GB",
   "video_count": "3349",
   "file_size": "1.14 GB",
   "file_count": "266",
   "other_size": "37.92 MB",
   "other_count": "52",
   "children": [
     {
       "filename": "វិទ្យាល័យ ព្រែកលាប",
       "file_meta": {
         "item_last_modify_date": "2023-02-13 04:23:52",
         "item_is_dir": true,
         "item_size": 4096,
         "item_mime_type": null
       }
     },
     {
       "filename": "STEM Contents",
       "file_meta": {
         "item_last_modify_date": "2023-02-03 18:23:48",
         "item_is_dir": true,
         "item_size": 4096,
         "item_mime_type": null
       }
     }
  ]
}
 ```

 |     Error    |             Body           |
 | ------------ | -------------------------- |
 |     None     | None                       |

 ---
</details>