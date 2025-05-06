# Vehicle Damange Detection App

This app let's you drag and drop an image of a car and it will tell you what kind of damage it has.
The model is trained on third quarter front and rare view hence the picture should capture the third quarter front or rare view of a car. 

![app](app_screenshot.jpg)

### Model Details
1. Used ResNet50 for transfer learning
2. Model was trained on around 1700 images with 6 target classes
   1. Front Normal
   2. Front Crushed
   3. Front Breakage
   4. Rear Normal
   5. Rear Crushed
   6. Rear Breakage
9. The accuracy on the validation set was around 84%

### Set Up

1. To get started, first install the dependencies using:
    ```commandline
     pip install -r requirements.txt
    ```
   
2. Run the streamlit app:
   ```commandline
   streamlit run app.py