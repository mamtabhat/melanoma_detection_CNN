Problem statement: To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.
The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.


The data set contains the following diseases:

  -Actinic keratosis
  -Basal cell carcinoma
  -Dermatofibroma
  -Melanoma
  -Nevus
  -Pigmented benign keratosis
  -Seborrheic keratosis
  -Squamous cell carcinoma
  -Vascular lesion

  Rescaling and Normalization
  - rescaled images to normalize pixel values between (0,1).
  - Optimizer - Adam

  - Model 1:
  - Epochs - 20
  - No augmentation

    Observed very less Validation and Test accuracy about 30%
    Observed a huge overfitting


  - Model 2
    - 20 epochs
    - Augmentation with random flip rotate and zoom
    - Optimizer - Adam

    - Val accuracy got better by 0.03. but overfitting persisted

  - Model3
    - epochs 30
    - Augmentor library used
    - Handled class imbalance by generating 500 image samples for every class

  - Observation
    - Val accuracy improved to 77% overfitting drastically reduced
    - Test accuracy was 43%
