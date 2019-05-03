# Project-1

Q)What are Channels and Kernels (according to EVA)?

Q)Why should we only (well mostly) use 3x3 Kernels?
A)when convolution is done with nxn kernal, the number of trainable parameters are nxn ( n to the power 2).
Since the number trainable parameters increase with n, we would ideally want the n to be as small as possible.

When an mXm image is convolved with a nxn kernal, the resultant resolution is (m-n+1)x(m-n+1).

when n =1, there is no change in the resolution on the convolved image.
when n=2, there is no sense of left, right with a 2x2 kernal.
when n=3, it is the ideal kernal interms of number of trainable parameters and to have a sense of left and right in the kernal.



Q)How many times do we need to perform 3x3 convolution operation to reach 1x1 from 199x199 (show calculations)
A)When mXm image is convolved with a 3x3 kernal, the resultant resolution is (m-2) X (m-2).
when convolution with 3x3 kernal is done on the resulant image, the resoluion is (m-(2x2))x(m-(2x2)).
Third time it is (m-(2x3))x(m-(2x3)) and so on.

Lets say that it takes n times convolution with 3x3 kernal for the resolution to reach 1x1,
then from the above statements,
m-(2xn) = 1

m-1 = 2xn

n = (m-1)/2.

when m = 199, 
n = (199 - 1)/2 = 198/2 = 99.
