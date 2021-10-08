# Tele-Ophthamological Retina Exams the Cheap and Effective Way 
## 3-D Printing, an App, and Diagnosing Diabetic Retinopathy Early

Author – nate walter

## Business Problem
In parts of rural India, the diagnosis of Diabetic Retinopthy (DR) can be a difficult undertaking. Equipment is large and bulky, and the people have no means of traveling to clinics to be tested. If caught early enough, there are options available to mitigate patients' suffering in the long term. The oDocs Fundus Adapter is a 3-D printed accessory that holds a 20 diopter lens which fits over a smart phone's camera. It makes capturing images of the retina in remote locations of the world easy and affordable. The retinal image can be run through the Machine Learning model in our app and a diagnosis returned to the Technician, then and there. This will increase the number of patients that can be reached and cut down on time between image-capturing, diagnosis, and treatment. 


## Data
The Data are a combination of 3 datasets. The first, and the genesis for the idea, comes from the APTOS 2019 Blindness Detection on Kaggle. Second, data was sourced from Indian Diabetic Retinopathy Image Dataset (IDRID), I used both the train and test sets for training the Model, since both were accompanied by labels and id's. Lastly, I used some resized images from the 2015 Kaggle competition combined with resized images from 2019.

[Link to 2019 APTOS, Kaggle Dataset](https://www.kaggle.com/c/aptos2019-blindness-detection/data)

[Link to IDRID dataset](https://ieee-dataport.org/open-access/indian-diabetic-retinopathy-image-dataset-idrid) # download Dataset Files B.

[link to 2015/2019 resized dataset](https://www.kaggle.com/benjaminwarner/resized-2015-2019-blindness-detection-images)

## Methods
The 5 classes were extremely imbalanced. It was found that the majority of retinal images had no Diabetic Retinopathy (labeled 0). So I decided to drop certain  rows and combine different columns to form new dataframes, eventually forming one final dataframe, evening out the classes. It was apparent that the best approach to making predictions on a retinal image would be to use a multi-class Neural Network model. This evolved into utilizing a pre-trained deep neural network (ResNet50_V2), while replacing the last layer with one tailored specifically to this project.   

## Results

The model (Omega) predicted Diabetic Retinopathy on previously-unseen retinal images with 83.9% accuracy, a whole percentage point higher than the previous model. In this iteration of the project, the Omega model is performing respectably. I have also crested the wave of saving one's model and its weights as hdf5. I am now going to tune the image augmentation and possibly tweek some of the top layers. I'm in hopes this will continue to improve the Model's accuracy. Keep in mind, we started at around 56% accuracy. Onward and upward. 

Omega-Model's Confusion Matrix

<img width="365" alt="Screen Shot 2021-10-08 at 12 43 25 AM" src="https://user-images.githubusercontent.com/66656063/136504558-5fcce1f2-8595-4f95-9ccd-6cc19d453bd2.png">


Omega-Model's Metrics

<img width="735" alt="Screen Shot 2021-10-08 at 12 43 42 AM" src="https://user-images.githubusercontent.com/66656063/136504578-e2479995-3e90-406d-8f94-ad5660712f9b.png">


## Recommendations
Based on the price/performance comparison of the oDocs Fundus Adapter to its more complex, expensive, and bulkier alternatives, conjoined with the accuracy of the Neural Network model, it is recommended that the use of The oDocs Adapter and image classification app be implemented in the field. 

## Limitations and Next Steps
Frankly, lack of time limited the accuracy of the current Neural Network. Since the goal is to provide preventative treatment quickly for those poor souls in areas who might not otherwise receive it, use of the winning model from the APTOS 2019 Kaggle competition in the app would be the best initial step to take. As mentioned in the presentation (see Captsone-Presentation.mp4 above) it could be beneficial to have Engineering departments at Universities focused on 3-D printing include the plans for the oDocs Fundus Adapter into their students' curriculum. 

## For Further Information

You're encouraged to see the Google Colab Notebook above (Eta_Model.ipynb), as well as the presentation [on YouTube](https://www.youtube.com/watch?v=KsNJlq3wPlE)

To see in depth plans for the app and the oDocs Adapter check out:


[The App's GitHub Link](https://github.com/IBM/tfjs-web-app#1-clone-the-repo)


[Odocs 3-D Printing Plans](https://odocseyecare.shop/pages/3d-print)


for further information, please contact nate walter at:  natejwalter@gmail.com






