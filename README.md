# ImageCaptionGenerator_DeepLearningProject

This project generates captions for images. The task here is to caption images using artificial intelligence, where when faced by an image the machine produces a human understandable sentence and the produced sentence is a valid description of the content of the image. To achieve this Deep Learning models such as CNN-LSTM models have been used. The models are trained on Flickr8k dataset which contains 8000 images, of which 6000 images are used for training and 2000 for testing/validation.

The main objective is to generate a sensual caption to a new image after training on the dataset.

## Generating captions for different images

#### 1. Clone the project
git clone the project into your local machine


#### 2. TestImages folder
Add the images you intend to test to this folder. The image file type is expected to be jpg.


#### 3. Open jupyter notebook 'Caption Generator for new image.ipynb'
In this file, below the heading *Generate Captions for images*, following changes are to be made

1. In this project two different feature extractors for pictures were used to train the model namely InceptionV3 and Xception. Both trained models have been saved. If you want to generate the description with InceptionV3 model then use the model as **model = load_model('InceptionV3_model.h5')**. Else if you want to generate the description with Xception model then use the model as **model = load_model('Xception_model.h5')**
2. Now we have give the image filename for which you intend to generate a caption. For the variable test_filename give the appropriate image path. Here we have added the test images to "TestImages" folder. If you have added an image with filename face_paint.jpg, then the test_filename should be given as **test_filename = 'TestImages/face_paint.jpg'**.

#### 4. Run the whole jupyter notebook 'Caption Generator for new image.ipynb'

After all the required changes are made to the notebook, run the entire jupyter notebook. The caption for the image will be generated.

#### 5. Testing for other images

Repeat step 2 and step 3 and now execute only the code block below the heading *Generate Captions for images*


## Training the model from scratch

#### 1. Download the dataset

Download the dataset from https://github.com/goodwillyoga/Flickr8k_dataset and place them in the same folder where there are jupyter notebooks

#### 2. Train the model

Open *Image Captioning - Training.ipynb*

As discussed above, two different feature extractors are used namely Xception and InceptionV3. Use them accordingly.
- In the extract features function, if you want to use InceptionV3 then say **model = InceptionV3(include_top=False, pooling='avg' )** or if you want to use Xception then say **model = Xception(include_top=False, pooling='avg' )**.
- Similarly, at the end before the plot, save the model accordingly. If you have used InceptionV3 model for feature extraction then say **model.save('InceptionV3_model.h5')**. Or if you have used Xception model for feature extraction then say **model.save('InceptionV3_model.h5')**

After making these changes run the entire notebook.


#### 3. Testing the model

Open *Image Captioning - Testing.ipynb*

Similar to the changes made in the training file, Use InceptionV3 or Xception according to what is used in the training file. If InceptionV3 is used for training, then use the InceptionV3 for testing as well. Same is the case with Xception.


#### 4. Generating Captions for different images

Follow the steps given at the start of this document to generate captions for different images.
