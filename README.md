# Training Generative Adversarial Networks with Limited Data #

This implementation follows the official NVIDIA research paper on training GANs with limited data, applied on the CIFAR-10 Dataset.

Since training GANs with limited data leads to overfitting and collecting large amounts of data (of order 1-10 million) is an extremely difficult task. With the help of the methods proposed in this paper, we can train GANs using as few as a thousand images.


![Alt text](./gen.jfif?raw=true "Generated Images")


### stylegan2-ada.ipynb ###
This notebook contins the whole code that was used to generate the required results. Firstly it mounts the google drive onto your colab/jupyter. And downloads the cifar-10 dataset on your Gdrive. Now running the first section gives us 30k generated images (here we have chosen 3000 images for each class). You can see these 32x32 images are very close to the class they are associated with.

- Open stylegan2_ada.ipynb in colab.research.google.com.
- Click on 'runtime' -> change runtime type-> hardware accelerator: GPU
- Ensure runtime is connected.
- Now click on 'runtime' and click ' run all'.

To further determine the code efficacy we have deployed a method to calculate metrics like FID and KID onto these 3000 images in each class and then we have plotted this data onto a bar chart. This gives us a rough idea that obtained range of FID as well as KID is well within the good range and hence the pretrained-network was able to generate almost real-like images for most classes.

![stylegan_fid](https://user-images.githubusercontent.com/101360312/233295092-9627e227-9f0a-4a6f-aa07-f9cd34932f0b.png)
![stylegan_kid](https://user-images.githubusercontent.com/101360312/233295140-82a0acd3-fd6d-4f88-992f-2eae1b8ee957.png)
