# Project-1

Q)What are Channels and Kernels (according to EVA)?

Q)Why should we only (well mostly) use 3x3 Kernels?

Q)How many times do we need to perform 3x3 convolution operation to reach 1x1 from 199x199 (show calculations)
A)When mXm image is convolved with a 3x3 kernal, the resultant resolution is (m-2) X (m-2).
when convolution with 3x3 kernal is done on the resulant image, the resoluion is (m-(2*2))x(m-(2*2)).
Third time it is (m-(2*3))x(m-(2*3)) and so on.

Lets say that it takes n times convolution with 3x3 kernal for the resolution to reach 1x1,
then from the above statements,
m-(2xn) = 1

m-1 = 2xn

n = (m-1)/2.

when m = 199, 
n = (199 - 1)/2 = 198/2 = 99.
