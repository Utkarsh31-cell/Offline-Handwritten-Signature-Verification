
Our Offline-Handwritten Signature Verification project consist of CEDAR Datasets and code of triplet loss with CNN using as resnet-50 as our architecture.

We have used dataset which is consist of 1320 genuine images amd 1320 forgery images.

We have 55 signers out of which each signers have 24 signatures in both genuine and forgery.

We have done work on Writer Independent Model in which we give training with dataset of genuine and forgery images and on testing with also both genuine and 
forgery images 

We have take seperate 11 signers  as our test dataset and remaining as training dataset.

Further we use Otsu threshold. so that those images which are above the threshold are considering as image under consideration 

Further we have normalize the image by taking image from  input in form of directory path as image and then firther convert it to 2d matrix form which pixels
wise  from.

After then we have normalize that from 0 to 1 form by taking upper limit as 255, since largest pixel has value  of 255.

Further we used triplet loss then after in which we use euclidian metric for calculatng the distance between two images.

Since as we know that triplet loss use margin which help it to seperate the positive to negative image seperate by distance.

This lead to differentiate the positive and negative  images form each other so that we can identify forgery and genuine signature.

it produces easy negative (unskilled forgery) and skilled forgery which is hard negative. 

Further sesy negative are just here psoitive and positive are base  and hard-negative are forgery images.

Further we have tensor matrix which is consist of similarity value so that we can compare similarity value which is most closest point if in positive 
it is closest i.e value(positive)>value(negatve) as closestness.we consider at in count as 1 and otherwise 0.

So number of  (count/total number of samples) are consider as our accuracy because we beleve that the all positive points are genuine but it predict only
count number of points are genuine points. 


