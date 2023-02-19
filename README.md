# CNN-ablation-study


### Objective


### Data

Famous dataset used for vision learning, PETS. 
Images of varying sizes of different animals
The images are named with the spesific animal's name and race(Model's target label), i.e cocker_spaniel_19.jpg


### Dataloader

#### Resize

To save on time and computing, allowing to run multiple models on more epochs

Hypothesis: Squish will perform well on square images

### Augmentation


Using crop and resizing method as mentioned before

Using btch_tfms to transform the pictures with a multiplier from 0 to 2.0

More info about augmentation, a good note book is [Introduction to Image Augmentation using fastai by Sanyam Bhutani](https://www.kaggle.com/code/init27/introduction-to-image-augmentation-using-fastai)

Dataloaders with multiplier with values 0.1, 0.5, 1.0, 1.5 and 2.0

Using Resnet18 with 10 epochs 

After 5 epochs augmented data performs better


