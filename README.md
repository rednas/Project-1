# Project-1

Q)What are Channels and Kernels (according to EVA)?                                                                         
A)In Deep learning, filters(Channels/Kernels) are used to extract features from the images. 
A filter basically is a nxn Matrics which will be used to do convolution operation on the image file to extract a feature out of the image.

For Example, when a channel that is meant of detecting vertical edges is used to do convolution on an image, in the resultant image, 
all the locations in the image where there are vertical edges, will have more pixel value(intense or more loud) and other location will not be loud or will have less pixel value.                                                                                           
Like wise a red colour detecting kernal will result in more intensity at all the locations in the image where there is red colour and at other locations the intensity of the pixel will be very less or zero.                                                                 

There are various types of filters namely High pass filter, low pass filter, Gaussian filter, etc.
Even though, the operation of convolution is same, the difference in the behavior of the filter or in other words the kind of feature that is extracted from the image, stems from the variation in the values of the Matrics.                                                 


Q)Why should we only (well mostly) use 3x3 Kernels?                                                             
A)when convolution is done with nxn kernal, the number of trainable parameters are nxn ( n to the power 2).                 
Since the number trainable parameters increase with n, we would ideally want the n to be as small as possible.                 

When an mxm image is convolved with a nxn kernal, the resultant resolution is (m-n+1)x(m-n+1).                               

when n =1, there is no change in the resolution on the convolved image.                                                             
when n=2, there is no sense of left, right with a 2x2 kernal.                                                                  
when n=3, it is the ideal kernal interms of number of trainable parameters and to have a sense of left and right in the kernal.



Q)How many times do we need to perform 3x3 convolution operation to reach 1x1 from 199x199 (show calculations)
A)When mxm image is convolved with a 3x3 kernal, the resultant resolution is (m-2) x (m-2).                                
when convolution with 3x3 kernal is done on the resulant image, the resoluion is (m-(2x2))x(m-(2x2)).                        
Third time it is (m-(2x3))x(m-(2x3)) and so on.                                                                               

Lets say that it takes n times convolution with 3x3 kernal for the resolution to reach 1x1,                                      
then from the above statements,
m-(2xn) = 1

m-1 = 2xn

n = (m-1)/2.

when m = 199, 
n = (199 - 1)/2 = 198/2 = 99.
