# QTM350_aws_project

Hello! This is team Vegetariana's github repo. 

We are testing AWS Rekognition's ability to recognize individuals from different image qualities. We will include our data, notebook, and process in this repo. AWS Rekognition is used by law enforcment and security industry so understanding how robust it is can have real world implications.

With the increased use of facial recognition and ML in Law Enforcement, understanding the biases that this software has and how it groups individuals by specific facial features can help us understand potential pitfalls of discriminatory or disproportionate law enforcement against specific marginalized groups. In this post, we hope to show whether or not Amazon Rekognition’s “compare faces” feature tends to have higher error rates with certain features and manipulations, describe the data collection and analyzation processes, and discuss why this may be problematic in real-world application as well as offer some potential solutions.
Amazon Rekognition and Discrimination


## Amazon Rekognition and Discrimination

According to this article from the ACLU, Amazon met up with ICE to discuss using Amazon Rekognition to “supercharge” deportation measures delegated by the Trump Administration. If Amazon Rekognition does, indeed, host biases against marginalized groups, a lot of people could be at risk for deportation or wrongful detention and apprehension. According to the ACLU:

In July, we released a test showing that Amazon Rekognition falsely matched 28 members of Congress with mugshot photos, with members of color incorrectly matched at a disproportionately higher rate.

These errors in Amazon Rekognition’s software and clear discriminatory biases could be disastrous for immigrants, communities of color, and protestors if implemented broadly.


## The Goal

To test our hypothesis that Amazon Rekognition is not free from discriminatory bias, we plan to manipulate a single image variable to test the response of the ML service’s “Detect Faces” feature across multiple images of a diverse group of people. We will supply one copy of each photo as it is and use an altered version of that same photo to see how confidently the ML service can match the images and recongize the gender, emotion, and age range. During the initial stages of this project, we plan to host a few experiments by comparing blurred versions of images compared to unblurred images.


## The Data Collection Process

To gather the images we used in this study, we relied on images of portraits supplied by an API. We want to test pictures of males and females in the same ethnic group and age range to minimize the confounding variables. We used about 150 pictures generated from the public API. The public API we’ve decided to go with is unsplash.com, which is a picture database that contains over 50k photos under the keyword “portrait.”

As seen through these images, there is a wide variety of ages, genders, ethnic groups, photo conditions, and emotions that we can see through these images. This allows us to have a large and varied sample size for our testing. The advantage of the API is the large amount of portraits available lets us pick and choose based on what variables we want to test, lowering the risk of confounding variables. If it is feasible, we could go further and test hundreds of pictures to improve the generalizability of our result. This allows us to find even more intricate details hidden in Rekognition’s software and allows us to see if there is any possible issues with bias. Our foremost goal is to extend our test variables to age range and ethnic groups and measure those effects on emotional accuracy.

Amazon prides itself on being accurate on these categories that we’re looking to test. Our goal is simply to measure the extent to which these claims are accurate, as, if Amazon is looking to implement this technology into Law enforcement, the margin of error should be minimal to avoid discrimination, stereotyping, or profiling.


## Data Metrics

To measure our three variables of interest; gender, emotion, and age range, we used Rekognition's confidence score of these three variables from the images we uploaded, both blurred and original, to measure the difference of the confidence scores on each altered image. Using these numbers, we can determine if Rekognition has a harder time telling the binary gender, emotion, and continuous age range of the faces in images that have been blurred. We hypothesize that indeed, Rekognition will have lower confidence in these variables for the blurred images.

To see if there is in fact a bias in these measurements across race, we constructed and manually entered a binary variable for each image: "white" and "non-white". In our analysis, we look at the confidence scores between these groups to see if there is a bias in Rekognition. We hypothesize all three variables will have higher confidence scores for the white group than the non-white group.

## WIP

## More Information
For a more detailed look at our project, please visit our blog using this link: https://emory.sharepoint.com/sites/QTM350Fall2020-Vegetariana/Shared%20Documents/Vegetariana/FinalBlog.html
