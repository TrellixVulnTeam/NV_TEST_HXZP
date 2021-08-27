# NV_TEST
## Requirements
```
conda env create -f env_config.yaml
conda activate nv_test
```
## Download pre-trained model
[pretrain_model](https://k00.fr/2zz6i2ce)
### COCO
Create a symlink `data/coco` containing the images from the 2017 split in
`train2017` and `val2017`, and their annotations in `annotations`. Files can be
obtained from the [COCO webpage](https://cocodataset.org/). In addition, we use
the [Stuff+thing PNG-style annotations on COCO 2017
trainval](http://calvin.inf.ed.ac.uk/wp-content/uploads/data/cocostuffdataset/stuffthingmaps_trainval2017.zip)
annotations from [COCO-Stuff](https://github.com/nightrome/cocostuff), which
should be placed under `data/cocostuffthings`.
### Train model
```
python main.py --base configs/coco_cond_stage.yaml -t True --gpus 0,
```
