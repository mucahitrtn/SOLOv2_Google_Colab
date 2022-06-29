## SOLOv2_Google_Colab
### Train SOLOv2 on custom dataset with google colab

#### Create data/mydataset folders under SOLO folder
<img src="Images/data_folder.png" alt="drawing" style="width:300px; height:270px"/>

#### Create my_dataset.py under mmdet/datasets
<img src="Images/mmdet_dataset.png" alt="drawing" style="width:300px; height:420px"/>

Inside my_dataset.py:

```py
from .coco import CocoDataset
from .registry import DATASETS
@DATASETS.register_module
class MyDataset(CocoDataset):
    CLASSES = ['Your', 'Classes', ...]
```

#### Under mmdet/datasets edit `__init__.py`
<img src="Images/init_py.png" alt="drawing" style="width:900px; height:600px"/>

#### Edit your config file.

##### Edit your number of classes 
<img src="Images/dataset.png" alt="drawing" style="width:600px; height:90px"/>

##### Edit dataset settings
<img src="Images/train_val.png" alt="drawing" style="width:600px; height:450px"/>


##### Runtime settings
<img src="Images/runtime_Settings.png" alt="drawing" style="width:600px; height:200px"/>
