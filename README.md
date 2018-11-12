# Malireddy-SparkWordCount
This is a Big Data Spark project repository.

## About Me & Objective
My name is Aditya Malireddy. I am a graduate student at Northwest Missouri State University studying Applied computer science. The objective of this project is to access the raw data and reorganize the collected date and to generate the word counts and frequently used words information.

## Data
I have chosen William Shakespeare's Romeo and Juliet Act 3 scene 1 as my data. I have copied the data to a text file(Romeo&juliet.txt) and used it.

[Romeo and Juliet](http://shakespeare.mit.edu/romeo_juliet/romeo_juliet.3.1.html)

## Commands Used

1. Commad to load the data 
> val inputFile = sc.textFile("C:/44517/Malireddy-SparkWordCount/Romeo&juliet.txt")

2. Command to count the words
> val counts = inputFile.flatMap(line => line.split(" ")).map(word => (word,1)).reduceByKey(_ + _);

3. Command to save the output results.
> counts.saveAsTextFile("c:/tmp/show-spark/Romeo&juliet_output")

## Result

| Word       | Count|
|---------   |------|
| MERCUTIO   | 18   |
| thou       | 22   |
| with       | 21   |
| I          | 30   |
| heads      | 30   |
| Juliet     | 30   |
| of         | 27   |
| for        | 19   |
| Citizens   | 19   |
| that       | 18   |
| the        | 46   |
| a          | 35   |
| to         | 22   |
| and        | 27   |

The above shown words are the most repeated words in the play. The most used word is "the" which is repeated 46 times and the next is "a" which is repeated 35 times.

## Graph

![wordcount_chart](https://user-images.githubusercontent.com/31738366/48321929-99307d80-e5ea-11e8-9451-c455aa930850.png)







