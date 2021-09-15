# Tele-Ophthalomical Retina Exams the Cheap and Effective Way 
## 3-D Printing, an App, and Diagnosing Diabetic Retinopathy Early

Author – nate walter

## Business Problem
In parts of rural India, the diagnosis of Diabetic Retinopthy (DR) can be a difficult undertaking. Equipment is large and bulky, and people have no means of traveling to clinics to be tested. If caught early enough, there are options available to mitigate patients' suffering in the long term. The oDocs Fundus Adapter is a 3-D printed accessory that holds a 20 diopter lens which fits over a smart phone's camera. It makes capturing images of the retina in remote locations easy and affordable. The retinal image can be run through the Machine Learning model in our app and a diagnosis returned to the Technician then and there. This will increase the number of patients that can be reached and cut down on time between image capture, diagnosis, and treatment. 


## Data
The Data are a combination of 3 datasets. The first, and the genesis for the idea, comes from the APTOS 2019 Blindness Detection on Kaggle. Secondly, data was sourced from Indiann Diabetic Retinopathy Image Dataset (IDRID), I used both the train and test sets to train on, since both were accompanied by labels and id's. Lastly, I used some resized images from the 2015 Kaggle competition combined with resized images from 2019.

[Link to 2019 APTOS, Kaggle Dataset](https://www.kaggle.com/c/aptos2019-blindness-detection/data)

[Link to IDRID dataset](https://ieee-dataport.org/open-access/indian-diabetic-retinopathy-image-dataset-idrid) # download Dataset Files B.

[link to 2015/2019 resized dataset](https://www.kaggle.com/benjaminwarner/resized-2015-2019-blindness-detection-images)

## Methods
The 5 classes were extremely unbalanced. It was found that the majority of retinal images had no Diabetic Retinopathy (labeled 0). So I decided to drop certain  rows and combine different columns into new dataframes to even out the classes. It was apparent that the best approach to making predictions on a retinal image would be to use a multi-class Neural Network model. This evolved into utilizing a pre-trained deep neural network (ResNet50_V2), while removing the last step and replacing it with our own.   

## Results

The model predicted Diabetic Retinopathy of previously-unseen retinas with 66% accuracy.

<img width="366" alt="Screen Shot 2021-09-15 at 2 25 39 PM" src="https://user-images.githubusercontent.com/66656063/133496733-5aaff67a-04fd-4451-a3a1-fa4738475940.png">


## Recommendations
Based on the price/performance comparison of the oDocs Fundus Adapter to its more complex and bulky alternatives, and the accuracy of the Neural Network model, it is recommended that the use of The oDocs Adapter and image classification app be implemented in the field. 

## Limitations and Next Steps
Frankly, inexperience is limiting the accuracy of the current Neural Network. Since the goal is to provide preventative treatment for those poor souls in areas who might not otherwise receive it, use of the winning model from the APTOS 2019 Kaggle competition in the app would be the best step to take. As mentioned in the presentation (see google slide deck above) it could be beneficial to have Engineering departments at Universities focused on 3-D printing include the plans for the oDocs Fundus Adapter into the curriculum. 

## For Further Information

You're encouraged to see the Google Colab Notebook above, as well as the presentation  ****include those hyperlinks??

To see in depth plans for the app and the oDocs Adapter check out:


[The App's GitHub Link](https://github.com/IBM/tfjs-web-app#1-clone-the-repo)


[Odocs 3-D Printing Plans](https://odocseyecare.shop/pages/3d-print)


for further information, please contact theeasyswing@gmail.com






