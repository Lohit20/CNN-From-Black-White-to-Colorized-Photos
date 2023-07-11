# CNN-From-Black-White-to-Colorized-Photos
1. Objective

The objective of our project is to create a fully automated method for generating realistic colorizations of black-and-white photographs and videos. By leveraging advanced computer vision techniques and deep learning models, we aim to accurately assign colors to grayscale images, resulting in visually appealing and lifelike colorized outputs.

2. Methodology

Our methodology involves the following steps:

Preprocessing: Convert the input black-and-white images/videos to a suitable format for colorization.
LAB Color Space: Utilize the LAB color space, which separates color information from the luminance channel, to perform colorization more effectively.
Caffe DL Model: Employ the power of deep learning by utilizing a Caffe DL Model trained on a large dataset to predict accurate color information for each pixel.
Post-processing: Apply techniques to refine and enhance the colorized output for better visual quality.

3. Analysis

We have found that the colorizing feature can also be used for correcting faded or otherwise uncorrectable color images. As an example, we experimented with an original image of singer Bekka Bramlett and saxophonist Deanna Bogart, which was taken under club lighting with only red and blue LEDs that could not be color corrected.

Our solution involved converting the image to monochrome using the Black and White adjustment layer, which resulted in a usable photograph. We then applied the Colorize Neural Filter to achieve the desired colorization.

4. Network Architecture

Our network architecture involves the use of a deep neural network (CNN) to transform black-and-white images into colorized photos. The output includes probability distributions for each pixel, with the top-left image representing the final prediction of our system. The distribution is quantized into blocks of the ab gamut, where high probabilities are displayed as higher luminance.

We analyzed different scenarios, such as predicting the background color of a bird, color variations for oranges, and the uncertainty of colors in a person's shirt and sarong. Despite the multimodality of the per-pixel distributions, the results, after taking the annealed mean, typically exhibit spatial consistency.

5. Conclusions

Colorizing images is a specialized form of graphics work and a challenging problem in computer vision. Through our research, we have demonstrated that employing deep neural networks (DNNs) can produce colorized results that are indistinguishable from real color photos.

By utilizing advanced techniques and models, we have achieved realistic and visually pleasing colorizations. Our project opens up opportunities for automating the colorization process, offering practical applications in various domains such as photography, restoration, and multimedia.

6. Future Work

While our current method is applicable for images, further refinement is required to make it suitable for video colorization. Manual intervention by an artist is necessary at the moment. However, we believe that with training on a larger dataset, the predictive power of the model would improve, leading to more consistent and accurate colorization results for videos.

By continuing research in this area and exploring larger datasets, we aim to enhance the applicability of our method and make it more accessible for real-world video colorization scenarios.
