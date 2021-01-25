# Generating Image segmentaion Masks form JSON files

This repo generates the segementation (instance/ semantic) masks from provided json files. Yor directory should be in following order

```
├── data
│   └── test_image.png
│   └── test_image.json
├── json2seg_masks.py
└── output
```

`data` contians your images and correspoding annotations. `output` dir where your `.png` masks will be saved.

## Data Generation

For custom datasets you can use [labelme](https://pypi.org/project/labelme/) to generate your own annotations. To install `labelme` type following in `cmd`

```
pip install labelme
```

You can label you data as follows,

![alt text](https://github.com/Mr-TalhaIlyas/Generating-Image-Segmentation-Masks-form-JSON-files/blob/master/screens/Screenshot%20(173).png)

## Sample usage

```python
num_classes = 2
class_name = ['mountain', 'car']
# set it to ture if you are generating masks for instance segementation.
instance_seg = False  # True or False
# dir to save output masks
output_dir = 'C:/Users/Talha/Desktop/output/'
# path to json files
file_paths = glob.glob(os.path.join('C:/Users/Talha/Desktop/data/', '*.json')) 
```

## Sample Output

If `instance_seg = False`

![alt text](https://github.com/Mr-TalhaIlyas/Generating-Image-Segmentation-Masks-form-JSON-files/blob/master/screens/img1.png)

if `instance_seg = True`

![alt text](https://github.com/Mr-TalhaIlyas/Generating-Image-Segmentation-Masks-form-JSON-files/blob/master/screens/img2.png)
