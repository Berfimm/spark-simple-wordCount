# spark-simple-wordCount
Count the occurrences of unique words in a text, using basic map reduce.

The first thing a Spark program must do is to create a SparkContext object, which tells Spark
how to access a cluster. To create a SparkContext, there is need to build a SparkConf object
that contains information about your application.

Spark revolves around the concept of a resilient distributed dataset (RDD), which is a fault-
tolerant collection of elements that can be operated on in parallel.
In this project I used the latter, external datasets.Read input text file using SparkContext variable and find number of lines in the file.

flatmap of words is created The words are type of PythonRDD. Each
line is splitted into words using “ “ as a separator. In the second line, each word is mapped to
key: value pair of word, 1. 1 is the number of occurrences. The result is reduced by key,
which is the word, and the values are added. Result is saved to a text file.


Words.txt file is taken as an input and number of occurrences of unique words in the text is
shown both as an output on ide and as a file.
