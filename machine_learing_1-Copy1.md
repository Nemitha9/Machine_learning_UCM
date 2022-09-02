```python
Question 1
The following is a list of 10 students ages:
ages = [19, 22, 19, 24, 20, 25, 26, 24, 25, 24]
    • Sort the list and find the min and max age
    • Add the min age and the max age again to the list
    • Find the median age (one middle item or two middle items divided by two)
    • Find the average age (sum of all items divided by their number)
    • Find the range of the ages (max minus min)
```


```python
ages = [19, 22, 19, 24, 20, 25, 26, 24, 25, 24]

## • Sort the list and find the min and max age

print(sorted(ages))

min_values = min((ages))
print(min_values)

max_values = max((ages))
print(max_values)

## • Add the min age and the max age again to the list

ages.append(min_values)
ages.append(max_values)

print(ages)

##  • Find the median age (one middle item or two middle items divided by two)
import statistics
print(statistics.median(ages))

##  • Find the average age (sum of all items divided by their number)

print(statistics.mean(ages))

## • Find the range of the ages (max minus min)

print(max_values - min_values)
```

    [19, 19, 20, 22, 24, 24, 24, 25, 25, 26]
    19
    26
    [19, 22, 19, 24, 20, 25, 26, 24, 25, 24, 19, 26]
    24.0
    22.75
    7



```python
Question 2
    • Create an empty dictionary called dog
    • Add name, color, breed, legs, age to the dog dictionary
    • Create a student dictionary and add first_name, last_name, gender, age, marital status,
skills, country, city and address as keys for the dictionary
    • Get the length of the student dictionary
    • Get the value of skills and check the data type, it should be a list
    • Modify the skills values by adding one or two skills
    • Get the dictionary keys as a list
    • Get the dictionary values as a list
```


```python
## • Create an empty dictionary called dog

dog = {}

## • Add name, color, breed, legs, age to the dog dictionary
    
dog["name"] = "data"
dog["color"] = "white"
dog["breed"] = "German"
dog["legs"] = "long"
dog["age"] = "1"

print(dog)

## • Create a student dictionary and add first_name, last_name, gender, age, marital status,
## skills, country, city and address as keys for the dictionary

student = {}

student["first_name"] = ""
student["last_name"] = ""
student["gender"]= ""
student["age"] = ""
student["marital_status"] = ""
student["skills"] = ["eating", "sleeping"]
student["country"] = ""
student["city"] =""
student["city"] = ""
student["address"] = ""

print(student.keys())

##  • Get the length of the student dictionary
print(len(student.keys()))

##  • Get the value of skills and check the data type, it should be a list
print((student["skills"]))

## • Modify the skills values by adding one or two skills

student["skills"].append("spending")
student["skills"].append("social_networking")
print(student["skills"])

## • Get the dictionary keys as a list

print([student.keys()])

##  • Get the dictionary values as a list

print([student.values()])
```

    {'name': 'data', 'color': 'white', 'breed': 'German', 'legs': 'long', 'age': '1'}
    dict_keys(['first_name', 'last_name', 'gender', 'age', 'marital_status', 'skills', 'country', 'city', 'address'])
    9
    ['eating', 'sleeping']
    ['eating', 'sleeping', 'spending', 'social_networking']
    [dict_keys(['first_name', 'last_name', 'gender', 'age', 'marital_status', 'skills', 'country', 'city', 'address'])]
    [dict_values(['', '', '', '', '', ['eating', 'sleeping', 'spending', 'social_networking'], '', '', ''])]



```python
Question 3
    • Create a tuple containing names of your sisters and your brothers (imaginary siblings are
fine)
    • Join brothers and sisters tuples and assign it to siblings
    • How many siblings do you have?
    • Modify the siblings tuple and add the name of your father and mother and assign it to
family_members
```


```python
## • Create a tuple containing names of your sisters and your brothers 

sisters = ("Aikya", "Nischitha")
brothers = ("Bezos","Leo")
print(sisters)
print(brothers)

## • Join brothers and sisters tuples and assign it to siblings

siblings = sisters + (brothers)
print(siblings)

## • How many siblings do you have?

print(len(siblings))

## • Modify the siblings tuple and add the name of your father and mother and assign it to
## family_members
family = siblings + ("father","monther")
print(family)

```

    ('Aikya', 'Nischitha')
    ('Bezos', 'Leo')
    ('Aikya', 'Nischitha', 'Bezos', 'Leo')
    4
    ('Aikya', 'Nischitha', 'Bezos', 'Leo', 'father', 'monther')



```python
Question 4
it_companies = {'Facebook', 'Google', 'Microsoft', 'Apple', 'IBM', 'Oracle', 'Amazon'}
A = {19, 22, 24, 20, 25, 26}
B = {19, 22, 20, 25, 26, 24, 28, 27}
age = [22, 19, 24, 25, 26, 24, 25, 24]
    • Find the length of the set it_companies
    • Add 'Twitter' to it_companies
    • Insert multiple IT companies at once to the set it_companies
    • Remove one of the companies from the set it_companies
    • What is the difference between remove and discard
    • Join A and B
    • Find A intersection B
    • Is A subset of B
    • Are A and B disjoint sets
    • Join A with B and B with A
    • What is the symmetric difference between A and B
    • Delete the sets completely
    • Convert the ages to a set and compare the length of the list and the set.
```


```python

it_companies = {'Facebook', 'Google', 'Microsoft', 'Apple', 'IBM', 'Oracle', 'Amazon'}
A = {19, 22, 24, 20, 25, 26}
B = {19, 22, 20, 25, 26, 24, 28, 27}
age = [22, 19, 24, 25, 26, 24, 25, 24]

## • Find the length of the set it_companies
print(len(it_companies))

##  • Add 'Twitter' to it_companies

it_companies.add("Twitter")
print(it_companies)

## • Insert multiple IT companies at once to the set it_companies

it_companies.update(["Norton", "HP", "FANNIE MAE"])
print(it_companies)

##  • Remove one of the companies from the set it_companies

it_companies.remove("Facebook")

print(it_companies)

##  • What is the difference between remove and discard

## Set discard () Python set discard () is a built-in method that removes an element from the set only if the item 
##is present in the set.

## remove throws an error if a given element is not presnet in the set

## • Join A and B

print(A.union(B))

##  • Find A intersection B

print(A.intersection(B))

## • Is A subset of B
print(A.issubset(B))
##  • Are A and B disjoint sets
print(A.isdisjoint(B))
##  • Join A with B and B with A
print(A.union(B))
print(B.union(A))
##  • What is the symmetric difference between A and B
print(A.symmetric_difference(B))
## • Delete the sets completely
A.clear()
print(A)
B.clear()
print(B)
## • Convert the ages to a set and compare the length of the list and the set.
print(len(list(age)))
print(len(set(age)))
```

    7
    {'Google', 'Amazon', 'Oracle', 'Apple', 'Microsoft', 'Twitter', 'IBM', 'Facebook'}
    {'Google', 'Amazon', 'Apple', 'FANNIE MAE', 'Microsoft', 'Oracle', 'Twitter', 'Facebook', 'HP', 'Norton', 'IBM'}
    {'Google', 'Amazon', 'Apple', 'FANNIE MAE', 'Microsoft', 'Oracle', 'Twitter', 'HP', 'Norton', 'IBM'}
    {19, 20, 22, 24, 25, 26, 27, 28}
    {19, 20, 22, 24, 25, 26}
    True
    False
    {19, 20, 22, 24, 25, 26, 27, 28}
    {19, 20, 22, 24, 25, 26, 27, 28}
    {27, 28}
    set()
    set()
    8
    5



```python
Question 5
The radius of a circle is 30 meters.
    • Calculate the area of a circle and assign the value to a variable name of _area_of_circle_
    • Calculate the circumference of a circle and assign the value to a variable name of
_circum_of_circle_
    • Take radius as user input and calculate the area.
```


```python
## • Calculate the area of a circle and assign the value to a variable name of _area_of_circle_    
r = 30
_area_of_circle_ = 3.14*r*r
print(_area_of_circle_)

## • Calculate the circumference of a circle and assign the value to a variable name of

_circum_of_circle_ = 2 * 3.14 * r
print(_circum_of_circle_)

## • Take radius as user input and calculate the area.

print("Enter the radus: ")
r = input()

area_of_circle = 3.14*r*r
print("Now the area of circle is: ", area_of_circle)

```


```python
Question 6
“I am a teacher and I love to inspire and teach people”
    • How many unique words have been used in the sentence? Use the split methods and set
to get the unique words.

```


```python
sen = "I am a teacher and I love to inspire and teach people"

print((set(sen.split())))
print(len(set(sen.split())))
```

    {'inspire', 'teacher', 'a', 'love', 'teach', 'am', 'to', 'and', 'I', 'people'}
    10



```python
Question 7
Use a tab escape sequence to get the following lines.
 Name Age Country City
 Asabeneh 250 Finland Helsinki
```


```python
print("Name\t Age\t Country\t City\t")
print("Asabeneh\t 250\t Finland\t Helsinki\t")
```

    Name	 Age	 Country	 City	
    Asabeneh	 250	 Finland	 Helsinki	



```python
Question 8 Use the string formatting method to display the following:
radius = 10
area = 3.14 * radius ** 2
“The area of a circle with radius 10 is 314 meters square.”
```


```python

radius = 10
area = 3.14 * radius ** 2
print("The area of a circle with radius {} is {} meters square.".format(radius, area))
```

    The area of a circle with radius 10 is 314.0 meters square.



```python
Question 9
Write a program, which reads weights (lbs.) of N students into a list and convert these weights to
kilograms in a separate list using Loop. N: No of students (Read input from user)
Ex: L1: [150, 155, 145, 148]
Output: [68.03, 70.3, 65.77, 67.13]
```


```python
print("enter number of students weight in Lbs by coma seperator ")

weight = input()
weights = weight.split(",")

print([int(i)*2.20 for i in weights])


```

    enter number of students weight in Lbs by coma seperator 
    1,2,3
    [2.2, 4.4, 6.6000000000000005]



```python
Question 10
The diagram below shows a dataset with 2 classes and 8 data points, each with only one feature
value, labeled f. Note that there are two data points with the same feature value of 6. These are
shown as two x’s one above the other.
1. Divide this data equally into two parts. Use first part as training and second part as
testing. Using KNN classifier, for K=3, what would be the predicted outputs for the test
samples? Show how you arrived at your answer.
2. Compute the confusion matrix for this and calculate accuracy, sensitivity and specificity
values. 

```


```python
#.  1 

import numpy as ab
from sklearn.model_selection import train_test_split
from sklearn.neighbors import KNeighborsClassifier
# Assigning features and label variables
# First Feature
x = ab.array([[1,0],[2,0],[3,0],[6,0],[6,0],[7,0],[10,0],[11,0]])
y = ab.array([0,0,1,1,1,0,0,0])

x_train, x_test, y_train, y_test = train_test_split(x,y,test_size= 0.6, random_state = 0, shuffle = False)



model = KNeighborsClassifier(n_neighbors=3)
model.fit(x_train, y_train)

y_predict = model.predict(x_test)
y_predict  
print(y_predict)


# 2
# Confusion matrix 
from sklearn import metrics
confusion = metrics.confusion_matrix(y_test, y_predict)
print(confusion)


# Let's check the overall accuracy.
print(metrics.accuracy_score(y_test, y_predict))

# Let's calculate Sensitivity, Specificity and accuracy with different probability cutoffs 

from sklearn.metrics import confusion_matrix

TP = confusion[1,1] # true positive 
TN = confusion[0,0] # true negatives
FP = confusion[0,1] # false positives
FN = confusion[1,0] # false negatives

## Accuracy 

print(0 + 1 / 1 + 3)


## Sensitivity

print(TP / float(TP+FN))

## Specificity 
print(TN / float(TN+FP))

```

    [0 0 0 0 0]
    [[3 0]
     [2 0]]
    0.6
    4.0
    0.0
    1.0



```python

```
