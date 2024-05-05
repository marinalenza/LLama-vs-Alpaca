# Lessons Learned - Llama vs. Alpaca

In this small project to develop an AI to classify pictures of Llamas and Alpacas, I've learned many things from data collection, labelling to CNN architecture.

## Motivation

In the summer of 2023, I was in a work day trip in the mountains and there were Alpacas there. While I could recognize them as Alpacas, nobody else could.

Now in 2024, while reviewing about CNN architecture, there was this famous example problem "Dogs vs. Cats". Humans can recognize dogs and cats, but they can't recognize alpacas and llamas, so I shouldn't I train an AI to do that?

## Challenge 1 - Data Collection and Labelling

For "Dogs vs. Cats", the images were collected from different sources, including pictures that people post of their pets in social media, and they were labelled by using Captcha.

For "Llamas vs. Alpacas", this was the biggest challenge. There are not as many pictures available online (not as many people have them as pets) and many of the pictures are mislabelled (alpacas as llamas, llamas as alpacas). Captcha wouldn't help for obvious reasons.

This lead to the dataset needed to be collected and labelled manually, which copnsequentely lead to an initial small dataset (less than 300 pictures vs more than 10.000 from "Dogs vs. Cats").

## Challenge 2 - CNN Architecture

Due to the simple and small dataset, the ML architecture does not need to be complicated. Additionally, since the threshold of how humans can recognize those animals is so low (less than 30% on a pool that I made on instagram), if I would get a higher accuracy I would consider a success.

A simple architecture was chosen, with 8 convolution filters and only one layer of those filters. By training with the data, fluctuating curves for both accuracy and loss metrics were found. Investigating deeper (aka. Stack Overflow, ChatGPT, Reddit), this comes from repetive data in the mini batches, which consequentely came from having a very small dataset.

An accuracy of 69.23% was obtained on the test data, very similar to the trained data accuracy.

## Next Steps

Data is the most important asset for an AI, so I am currently working on collecting and labelling more pictures.
