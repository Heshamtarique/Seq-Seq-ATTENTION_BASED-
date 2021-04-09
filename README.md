## Sequence to Sequence model using ATTENTION mechanism
### in this tutorial we are going to do language modelling more precisely language translation. Data has been directly downloded from GOOGLE API. 
### our task is to use an architecture that can translate a sentance in spanish to an english sentance. The best suited architecture can be ENCODER-DECODER. But for feeding the data to this model we need to process it - some of the textual processing techniques were utilized here (for removal of punctuation mark, hashtags etc using regular expressions, removal of extra spaces is done using "strip" function). we get the processed spanish and english sentances. 
### Now the last work before feeeding the data to the model is -- encoding of the words. we will convert it into VECTOR OF DESIRED LENGTH called word EMBEDDING [we took 256], this can be sparse or dense generally dense is choosen as it has more meaning into it. 
### Now we can pass the different criteria needed for traning and testing purpose such as Batch_Size = 64, epoch =10 in each place, units =1024 dimensionality of the output space of RNN, Optiimizer= ADAM. 
### Training is done using three techniques--    training sequence to sequence WITHOUT ATTENTION, training sequence to sequence with DOT-PRODUCT ATTENTION, training sequence to sequence with BAHDANAU ATTENTION MECHANISM which performs best here in our translation task.
  ![Screenshot 2021-04-09 at 12 52 38 AM](https://user-images.githubusercontent.com/63514840/114207244-cc24fa00-9979-11eb-9f8e-b7a5dca9bc9c.png)
## plot of the validation loss can be seen below
# ![Screenshot 2021-04-09 at 9 40 08 PM](https://user-images.githubusercontent.com/63514840/114209520-52dad680-997c-11eb-93da-d8309f4a83f2.png)
