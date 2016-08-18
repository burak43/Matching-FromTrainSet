 This is a sample on matching descriptors detected on one image to descriptors detected in image set.
 So we have one query image and several train images. For each keypoint descriptor of query image
 the one nearest train descriptor is found the entire collection of train images. To visualize the result
 of matching we save images, each of which combines query and train image with matches between them (if they exist).
 Match is drawn as line between corresponding points. Count of all matches is equel to count of
 query keypoints, so we have the same count of lines in all set of result images (but not for each result
 (train) image).


Format:

./matching_to_many_images [detectorType] [descriptorType] [matcherType] [queryImage] [fileWithTrainImages] [dirToSaveResImages]


Example:

./matching_to_many_images SURF SURF FlannBased ./query.png ./train/trainImages.txt ./res/


NOTE: Unfortunately, it doesn't work for SURF and SIFT types. Try with ORB, if you want to see it works!
