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

Surprising how bad efficinet is performing


## The ablation study

### Resnet26

From the early testing, resnet26 seems to perform the best. Will be chosen as the benchmark.

### Augmentation impact

#### Resize 80

<img width="1089" alt="bilde" src="https://user-images.githubusercontent.com/54356437/222142744-8c3deb0a-e869-4c12-9aaa-fc52a573e27e.png">

![bilde](https://user-images.githubusercontent.com/54356437/222142283-608e1ec5-f180-4c65-b80f-17c4c86593b8.png)


### Resize 128 lowering architecture 

<img width="955" alt="bilde" src="https://user-images.githubusercontent.com/54356437/222101474-a8991f8a-0f32-41ce-9159-09ae20503dfc.png">

| resnet26 | resnet18 |
| --- | --- |
| ![bilde](https://user-images.githubusercontent.com/54356437/222100289-5a28c7c2-de56-414c-8a10-27871d8e142b.png) | 
![bilde](https://user-images.githubusercontent.com/54356437/222101088-ba55062a-1221-4e28-bfa6-31ed5e7f0efb.png)|


Dihedral

<img width="754" alt="bilde" src="https://user-images.githubusercontent.com/54356437/222100516-5cc81a2b-9976-462a-96c4-69fbffd8154b.png">



