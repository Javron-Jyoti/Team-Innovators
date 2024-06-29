# Team-Innovators
First we have applied a dehazing model using opencv and numpy which will dehaze the image according to the environmental conditions like foggy,rainy,dark,heavy sunlight,smoke etc. This is named as Image_Videodehazing.py
Then we used yolov8m.pt model to detect objects by iterating a loop through all the selected classes showed in classes.txt file and the loop is in data.yaml file.
After that we train our model in anaconda prompt by setting an epochs of first 200 then 500 and it only stopped early at first 35 then 65 epochs .
Then we predicted our trained model taking some random test data which showed an f1 score of 
