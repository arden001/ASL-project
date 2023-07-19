# ASL Detector

 My project is an ASL alphabet detector. I wanted to make this project because I actually have a deaf cousin, but due to my lack of knowledge of ASL, we have a difficult time communicating. I made this detector to aid in helping people learn/translate the basic foundation of ASL: the alphabet. With my project, I hope that it can turn into somehting bigger and better that will break down the communication barrier between the hearing and hearing impaired. I would love for this project to be able to detect full on ASL conversations and translate them!
 
## The Algorithm

This project depended on the Jetson Nano and python code was used in Visual Studio Code. To get this project to work, I had to find/create a dataset then download it into the jetson-inference directory. I then re-trained my network to process and detect the dataset. I used imagenet to detect what the hand sign was and output the percentage of what the letter was. 

## Running this project
1. Download a dataset OR create your own
2. Navigate to the jetson-inference directory
3. Navigate to /python/training/classification/data and add a directory into there (I used "asl_dataset")
4. Download the data into the asl_dataset
5. Create labels to sort the data into (i.e.: "a", "b")
6. Create train, val, and test folders
7. Split the data into the folders (train 70% , val 15% , test .15%)
8. Train the model
9. Export the network
10. Use the imagenet program
11. Set Net and Dataset variables
12. Run this command to see how it operates on an image: imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt data/asl_dataset/test/a/(NAME OF IMAGE) $DATASET/test/a/output.jpg
                        - Replace "NAME OF IMAGE" with image name

[View a video explanation here](video link)
