1. Labeled json data provided by AI HUB didn't fit the format required by detectron2, so data conversion is required.
   * To solve this problem, we defined "convert_json_files()"

2. GPU runtime error occurred.
   * To train the model, you have to prepare the NVIDIA GPU and its driver.
   * Or you can just handle this error with changing the runtime type in google colab



### Ver 1.0 - Error and Solution
1. JSON file error
* The format of the original JSON file didn't fit the Detectron2 model. As the model requires COCO dataset, the JSON file had to be modified.
* To solve this problem, we defined "convert_json_files()".

2. Merge Data Folder


3. GPU Runtime Error
* To train the model, you have to prepare the NVIDIA GPU and its driver.
* Or you can just handle this error with changing the runtime type in google colab 
