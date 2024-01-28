# How mucho are my mom and I alike?

## Problem:
Throughout my life, many people have often confused me with my mom, highlighting a strong physical resemblance between us. This frequent mix-up sparked my curiosity: just how much do we actually look alike? To answer this, I propose a unique challenge of quantifying our physical similarity through technological means.

The core of this problem lies in developing a reliable and accurate method to measure and compare facial features and characteristics in photographs. The complexity is further heightened by factors like age difference, changes in appearance over time, and variations in photo quality and conditions.

To tackle this, I aim to create and train a machine learning model using a collection of photographs of my mom and me. This model will analyze various aspects of our facial features, expressions, and other physical traits to determine a 'similarity score'.

In this first phase the model will recongice photos of both of us, but the idea is that I could use this inside an app so people could check how much are they alike to their mothers. 

##Solution 

In this project, 'How much are my mom and I alike?', we've developed a machine learning solution to quantitatively analyze and compare the physical resemblance between my mother and me. Utilizing a collection of our photographs, we've implemented facial recognition and comparison algorithms in a Google Colab notebook

The model, in its current state, predicts incorrectly about one-third of the time. This level of accuracy is notably similar to the frequency at which even family members mistake photos of my mom and me. The model's current performance can be attributed primarily to the limited dataset – a larger collection of photos would likely improve its accuracy. This parallel between the model's error rate and human error illustrates a significant point: the challenge of distinguishing between my mom and me is not just a computational issue but also a human one. As the model is refined with more data, we expect its accuracy to surpass human judgment, showcasing the capabilities of AI in nuanced tasks like facial recognition among closely related individuals.

## Train Results
Model achieved 0.33% error and 66.6% accuracy on the validation set.

<img width="367" alt="Screenshot 2024-01-21" src="https://github.com/Yosolita1978/screenshoots/blob/main/2024/AI/Screen%20Shot%202024-01-27%20at%201.59.23%20PM.png?raw=true">

You can get a good sense for the overall performance of the model using this confusion matrix. Darker colors correspond to larger numbers here, which suggests that our model is quite good at detecting me, but my mom is sort of a mixed bag.


## Usage
Model achieved 0.33% error

<img width="367" alt="Screenshot 2024-01-21" src="https://github.com/Yosolita1978/screenshoots/blob/main/2024/AI/Screen%20Shot%202024-01-27%20at%203.35.55%20PM.png?raw=true">

If we throw my model into the Classification Interpreter object, and take look at the top losses we will see that it has mostly problems classifying my mom. These seem a bit more reasonable to my trained eye.

As the model is refined with more data, we expect its accuracy to surpass human judgment, showcasing the capabilities of AI in nuanced tasks like facial recognition among closely related individuals.

Model achieved 0.33% error

<img width="367" alt="Screenshot 2024-01-21" src="https://github.com/Yosolita1978/screenshoots/blob/main/2024/AI/Screen%20Shot%202024-01-27%20at%204.38.33%20PM.png?raw=true">

In an interesting instance during our model's testing, it confused me for my mom in one of the photographs. Remarkably, this specific misidentification mirrored a real-life situation: my aunt, who is my mother's older sister, made the same mistake when viewing this photo. This occurrence highlights the model's realistic performance in replicating human perception, even mirroring errors made by those closest to us. It demonstrates the nuanced challenge of distinguishing between closely related individuals, a challenge that both our AI model and humans experience similarly.

# Next Steps
My next phase in this project aims to evolve the model from simply classifying photos as either mine or my mom's to quantifying our resemblance in a more nuanced way. The goal is to develop a feature where the model provides a percentage score indicating how much we resemble each other in each photo. This will involve enhancing the model's capability to analyze and compare specific facial features in greater depth, thereby providing a more detailed measure of similarity. 