# ImageCaptionGenerator_DeepLearningProject

This project generates captions for images. In order to test the project with different images, following steps are to be followed.

## Testing with different images

### 1. Clone the project
git clone the project into your local machine


### 2. TestImages folder
Add the images you intend to test to this folder. The image file type is expected to be jpg.


### 3. Open jupyter notebook 'Caption Generator for new image.ipynb'
In this file, below the heading *Generate Captions for images*, following changes are to be made

1. In this project two different feature extractors for pictures were used to train the model namely InceptionV3 and Xception. Both trained models have been saved. If you want to generate the description with InceptionV3 model then use the model as **model = load_model('InceptionV3_model.h5')**. Else if you want to generate the description with Xception model then use the model as **model = load_model('Xception_model.h5')**
2. Now we have give the image filename for which you intend to generate a caption. For the variable test_filename give the appropriate image path. Here we have added the test images to "TestImages" folder. If you have added an image with filename face_paint.jpg, then the test_filename should be given as **test_filename = 'TestImages/face_paint.jpg'**.

### 4. Run the whole jupyter notebook 'Caption Generator for new image.ipynb'

After all the required changes are made to the notebook, run the entire jupyter notebook. The caption for the image will be generated.

### 5. Testing for other images

Repeat step 2 and step 3 and now execute only the code block below the heading *Generate Captions for images*
