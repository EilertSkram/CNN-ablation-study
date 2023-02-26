# CNN-ablation-study


### Objective


### Data

Famous dataset used for vision learning, PETS. 
Images of varying sizes of different animals
The images are named with the spesific animal's name and race(Model's target label), i.e cocker_spaniel_19.jpg


### Dataloader

#### Resize

To save on time and computing, allowing to run multiple models on more epochs

![bilde](https://user-images.githubusercontent.com/54356437/219981106-9715973d-a1c6-470c-b1ab-ca40f783d57d.png)


Hypothesis: Squish will perform well on square images

### Augmentation


Using crop and resizing method as mentioned before

Using btch_tfms to transform the pictures with a multiplier from 0 to 2.0

More info about augmentation, a good notebook is [Introduction to Image Augmentation using fastai by Sanyam Bhutani](https://www.kaggle.com/code/init27/introduction-to-image-augmentation-using-fastai)

Dataloaders with multiplier with values 0.1, 0.5, 1.0, 1.5 and 2.0

Using Resnet18 with 10 epochs 

![bilde](https://user-images.githubusercontent.com/54356437/219981122-dc011ed0-2a44-481f-aae0-a3b00eaf1824.png)

After 5 epochs augmented data performs better


### Architecture

Used [Jeremy Howard's Notebook](https://www.kaggle.com/code/jhoward/which-image-models-are-best/) to find different architectures to try out

Limited which models avalible due to computing power and image size

Exploring the different levels of resnet-architectures, but including one model from different architecture
![bilde](https://user-images.githubusercontent.com/54356437/221413145-ca330c7e-d200-4f3b-b207-35d51e893658.png)

Surprising how bad 

