# SUN-RGBD-IS
A dataset converted from SUN-RGBD into COCO-style instance segmentation format

Train : 2838 images

Val : 946 images

Classes : 18

Resolution : 730 × 530


## Data preparation
https://drive.google.com/drive/folders/1R0MZIZbjH17hV4wWoI_D2mJqvheEG-5M?usp=sharing

```
SUNRGBD/
└── train/
    └── color/
└── val/
    └── color/
└── annotations/
    └── instances_train.json
    └── instances_val.json
└── train_depth/
└── train_depth_raw/
└── val_depth/
└── val_depth_raw/
```

## Data Format
```
annotation{
    "id": int,
    "image_id": int,
    "category_id": int,
    "segmentation": [polygon],
    "area": float,
    "bbox": [x,y,width,height],
    "iscrowd": 0 or 1,
}

categories[{
    "id": int,
    "name": str,
    "supercategory": str,
}]
```
