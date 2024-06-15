
| Version | History | Date |
|---------|---------|------|
| 1.0 | create | 2024.06.15 |


### Ver 1.0 - Error and Solution
1. JSON file error
* The format of the original JSON file didn't fit the Detectron2 model. As the model requires COCO dataset, the JSON file had to be modified.
* To solve this problem, we defined "convert_json_files()".

2. Merge Data Folder


3. GPU Runtime Error
