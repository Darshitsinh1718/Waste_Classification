# Waste_Classification


In this we use ImageDataGenerater for Data splitting and preprocessing


Data Augmentation -> Artificially creating new image from existing image 

augmentation we will used ,

rotation_range = 20 means rotate image  +-20 degree 

width_shift_range = 0.1 means move image horizontally 

height_shift_range = 0.1 means move image up and down 

zoom_range = 0.2 means close and far look for object 

horizontal_flip = True means left->right 


first we make train and validation data generator and then with the help of flow_from_directory load 
the data from dataset using path and write other feature

there are some problem which we care at preprocessing are rescale, reshape, small dataset for any 
class, two classes which are look like same (glass and plastic), background bias ,small dataset



In this we use mobilenet2 base model and add some layer for better accuracy.


after training we save model in database using this,
model.save("/kaggle/working/waste_model.h5")

We use gradio so we can see good input and output 
this will direct show in output section.
