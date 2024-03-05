# SUN-RGBD-IS
A dataset converted from SUN-RGBD into COCO-style instance segmentation format


![image](./img/img1.jpg)

```
SUN-RGBD-IS
Train   : 5070 images
Val     : 4872 images
Classes : 18
Size    : 730 × 530
Sensor  : Kinect V1, Kinect V2, Intel Realsense, Asus Xtion
```

We have exclusively converted the data acquired from SUN-RGBD using Kinect v2
```
SUN-RGBD-IS-kv2
Train   : 2838 images
Val     : 946 images
Classes : 18
Size    : 730 × 530
Sensor  : Kinect V2
```
## Data preparation

SUN-RGBD-IS : https://api.onedrive.com/v1.0/shares/u!aHR0cHM6Ly8xZHJ2Lm1zL3UvcyFBdFEycWtVUmI4dlFybU5aUmN3enVISU5McDRFP2U9WTV0UjFQ/root/content

SUN-RGBD-IS-kv2 : https://api.onedrive.com/v1.0/shares/u!aHR0cHM6Ly8xZHJ2Lm1zL3UvcyFBdFEycWtVUmI4dlFybVR3bC0yYUNpVHIySXc4P2U9ZFI2RzBw/root/content

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
