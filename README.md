## Add .gitignore file
```bash
curl https://raw.githubusercontent.com/JotiRoy01/general_template/main/.gitignore > .gitignore
```
## Downlaod init_setup.sh file using curl command
```bash
curl https://raw.githubusercontent.com/JotiRoy01/general_template/main/init_setup.sh > init_setup.sh
```
## Tensorflow Verification
```bash
python -c "import tensorflow as tf;print(tf.config.list_physical_devices('CPU'))"
``` 
# Installation of Object Detection API

## create TensorFlow Directory
```bash
mkdir TensorFlow && cd TensorFlow
```
## Clone The TensorFlow models folder here
```bash
git clone https://github.com/tensorflow/models.git
```
remove .git directory of models repository to avoid git conflicts
add models folder to .gitignore

add models folder to .gitignore
```bash
echo "TensorFlow/models" >> .gitignore
```
## Download protoc 
- https://github.com/protocolbuffers/protobuf/releases

## Add protoc builder.py file
```bash
curl https://raw.githubusercontent.com/protocolbuffers/protobuf/main/python/google/protobuf/internal/builder.py > env\Lib\site-packages\google\protobuf\internal
```
## Message "note: This error originates from a subprocess, and is likely not a problem with pip"
```bash
pip install pyodbc
```

- Unzip into root folder and add '<PATH TO path folder>/bin' into system environment variables

- run The following command
```bash
cd TensorFlow/models/research
protoc object_detection/protos/*.proto --python_out=.
```
## Install COCO API
```bash
pip install git+https://github.com/philferriere/cocoapi.git#subdirectory=PythonAPI
```

## Install Object Detection API

```bash
cp object_detection/packages/tf2/setup.py .
python -m pip install .
```
## Check packages install or not
```bash
pip freeze
pip freeze | grep <packagesname>
 ```

## Test your Installation - 
```bash
python object_detection/builders/model_builder_tf2_test.py
```

## Run example
- Create workspace/example_1 directory in project root
 ```bash
 mkdir -p workspace/example_1
 cd workspace/example_1
 ```
- Download notebook
```bash
curl https://tensorflow-object-detection-api-tutorial.readthedocs.io/en/latest/_downloads/55b1ed8e083cbc9ca3bfc1c18eb6b860/plot_object_detection_saved_model.ipynb > plot_object_detection_saved_model.ipynb
```