# <p align="center"> Vocal Fold </p>

> Muticlass Vocal Fold Image in Laryngoscopy: Blur image, No vocal fold, Normal vocal folds, benign lesion, malignant lesion

-------------------------------------------------------
# :pencil: Instructions

### Installation
- Go to root folder, run `pip install -e .`

### To adapt for personal project
1. Create your own dataset, dataloader, model, loss function, metric function, ... and register it to the registry so that it can be generated from config at runtime.
2. Customize inherited trainer and pipeline to your need, such as what to do before/after training/validating step,...
3. Modify configuration file

*See ```theseus/classification``` for example*

### To execute scripts with arguments
- Run the script with `-c` flag with specified config file. Example:

```
python train.py -c pipeline.yaml
```

- To override arguments inside the .yaml file, use flag `-o` with key and value. For example, to train 50 epochs and resume training from checkpoints:

```
python train.py \
    -c pipeline.yaml \
    -o trainer.args.num_iterations=5000 \
    global.resume=checkpoint.pth
```
**Notice: There are no spaces between keys and values in -o flag**

- Also, if you want to do inference, you need to write your own script. For example see ```configs/classification/infer.py```

# :school_satchel: Resources
- Example colab notebooks for classification tasks: [![Notebook](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1mZmT1B5zI1j_0w1MbP-kq8_Tbcx_tIFq?usp=sharing)
- Example colab notebooks for semantic segmentation tasks: [![Notebook](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1VlR1JolMmEX2OtNLvzfnHhHAfI4lJ-Qo?usp=sharing)

# :blue_book: References
- This repo is inspired by https://github.com/vltanh/torchan <span style="color:yellow"> **Remember to give it a star** </span>.
- The big refactor is mostly adapted from https://github.com/HCMUS-ROBOTICS/ssdf-nncore 's nncore, **which also deserves stars**.
