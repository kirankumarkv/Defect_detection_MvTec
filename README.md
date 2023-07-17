# Defect_detection_MvTec
Defect detection using Zero shot, Zero shot plus attributes and Few shot methods
1. Dataset Preparation:
  a.Download the MVTec AD dataset from the official website (https://www.mvtec.com/company/research/datasets/mvtec-ad/ ) and set up the dataset structure.
  b.Preprocess the dataset by resizing the images to a uniform size (e.g., 256x256) and applying any necessary data augmentation techniques to enhance the model's    performance. Low Accuracy: 0.31746031746031744

2. Zero-Shot Learning:
   Implement a zero-shot learning approach to classify the defects in the images.
   Divide the dataset into training and testing sets.
   Designed a novel approach that leverages pre-trained model resnet50 to achieve zero-shot defect classification
Result: Accuracy is too low
Zero-shot code file zero_shot.ipynb

3. Mutiple class carpet, capsule, bottle, hazelnut from mvtec_anomaly_detection are utilized to detect defects. 
Since it has multiple low detection of defects, the accuracy is low. Accuracy: 0.2417

4. Zero-Shot Learning + external knowledge (e.g., attributes, textual descriptions)
     to achieve zero-shot defect classification, attributes of capsule defects like 'crack', 'faulty_imprint', 'poke', 'scratch', 'squeeze' are given to attribute_classifier. some of the defect attribute chosen are
   defect_attributes = {
    'crack': ['visible', 'thin', 'narrow'],
    'faulty_imprint': ['misaligned', 'distorted', 'uneven'],
    'poke': ['deep', 'sharp', 'small'],
    'scratch': ['visible', 'linear', 'surface'],
    'squeeze': ['deformed', 'compressed', 'misshapen']
}
Accuracy increased drastically, Accuracy: 0.6325

5. The pre-trained resent is downloded using URL
   https://www.kaggle.com/datasets/mhiro2/pytorch-pretrained-models?select=resnet50-19c8e357.pth
   
