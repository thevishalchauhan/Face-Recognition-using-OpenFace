# Face-Recognition-using-OpenFace

## Creating Embedding of Faces
- Under Dataset Folder : Make a folder name is treated as a label and place atleast 10-20 images of the particular person for better accuracy.
- Command : python extract_embeddings.py --dataset dataset --embeddings output\embeddings.pickle --detector face_detection_model --embedding_model openface_nn4.small2.v1.t7

## Training Model
- Command : python train_model.py --embeddings output\embeddings.pickle --recognizer output\recognizer.pickle --le output\le.pickle

## Face Recognition 
-  Command : python recognize.py --detector face_detection_model --embedding_model openface_nn4.small2.v1.t7 --recognizer output\recognizer.pickle --le output\le.pickle --image images\inputImage

## Face Recognition - Video
- Command : python recognize_video.py --detector face_detection_model --embedding_model openface_nn4.small2.v1.t7 --recognizer output\recognizer.pickle --le output\le.pickle
