# Insight Data Engineer Project

## Project Idea

Match products with ideas, match ads with content.

## Purpose & use cases

When selling a products, making up a beautiful story is usually quite important, but it is not always easy for marketing department to come up with a nice story to tell. Even for the same product, people in different countries would care about different aspects. For exampele, when buying an air condition, the US customer might care more about how cold the outcome wind could be, while Chinese customer might pay more attention to its air-purify functions. As a result, telling the right story to the right customers becomes the crucial part. It also applies to advertise placement, showing an AC with an air-cleaning story on an air pollution news webpage is highly possible to attract more clicks. This project is designed to advise relevant ideas to any entities by extracting similarities from Common Crawler corpus. 

## Technologies

Amazon S3, Spark, Cassandra, Spark MLlib, Flask

## Achitecture

The raw data is stored in Amazon S3, it will be processed by Spark to translate ip address to location information, and to remove irrelevant field, as well as stop words and punctuations. after cleaning and tokenization, the dataset is stored in Cassandra then passed to Spark MLlib to form high-dimension matrices for different locations, where each word is represented as a vector. When users query specific word from the frond-end, the most related words will be returned and shown on the map.
