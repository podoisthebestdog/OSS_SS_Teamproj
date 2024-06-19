### 1. JSON file error
* Labeled json data provided by AI HUB didn't fit the format required by detectron2, so data conversion is required.
* To solve this problem, we defined "convert_json_files()".

### 2. GPU Runtime Error
* To train the model, you have to prepare the NVIDIA GPU and its driver.
* Or you can handle this error with changing the runtime type in google colab 
