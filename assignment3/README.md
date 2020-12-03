# AI6127: Assignment 3

Topic: Subword Models

## Q1: Subword Models

+  Modify the model of Question 3 of Tutorial 10 “Subword models” to replace the character embeddings with Byte Pair Encoding (BPE) for wordpiece model [30 marks]
  + You may consider to use BPE implementation mentioned in the lecture slides (https://github.com/rsennrich/subword-nmt) or to implement your own BPE [10 marks]
  + Follow the same filesystem for data as in the tutorial
  + If the BPE implementation requires any libraries other than those for the tutorial notebook, give clear instruction of how to install them [5 marks]
    iv. Give clear descriptions of which sections and cells are modified or added for what purpose [5 marks]
  + Report the resultant ‘test loss’ and ‘test accuracy’ with different target vocabulary sizes (e.g. 1000, 3000, 10000) and discuss comparison with the test results of Question 3 of Tutorial 9 [10 marks]

+ Modify the model with BPE for sentencepiece model [20 marks]
  + Implementation [10 marks]
  + Give clear descriptions of which sections and cells are modified or added for what purpose [5 marks]
    iii. Compare test results with wordpiece model, varying target vocabulary sizes (e.g. 1000, 3000, 10000), and discuss the comparison results [5 marks]
+ Submit the revised Jupyter notebook, renaming the notebook as ‘assignment3- [Name].ipynb’. If you implement wordpiece and sentencepiece models in two separate notebooks, submit both notebooks, renaming them as ‘assignment3- wordpiece-[Name].ipynb’ and ‘assignment3-sentencepiece-[Name].ipynb’, respectively



## References

Alexandra Birch Rico Sennrich Barry Haddow. Subword Neural Machine Translation. https://github.
com/rsennrich/subword-nmt. 2016.

John Richardson Taku Kudo. SentencePiece. https://github.com/google/sentencepiece. 2018.