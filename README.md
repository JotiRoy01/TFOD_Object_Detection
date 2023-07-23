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
