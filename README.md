# python-internship-task_10

1.Write a Python program for all the cases which can check a string contains only a certain set of characters (in this case a-z, A-Z and 0-9).

import re

print(bool(re.match("^[A-Za-z0-9]*$",'taskno10')))

print(bool(re.match("^[A-Za-z0-9]*$",'completed')))

2.Write a Python program that matches a word containing 'ab'.

import re

test_1 = "absolutely"

test_2 = "no word found"

def check(str) :

    regex = re.compile("ab+\w*")

    found = regex.findall(str)

    if len(found) != 0 : 

        for word in found : 

            print(word)

    else : 

        print("No word starts with 'ab'")

check(test_1)

check(test_2)

3.Write a Python program to check for a number at the end of a word/sentence.

import re

def check(str):

    regex = re.compile(".*[0-9]$")

    if regex.findall(str):

        print("number at the end of string!!")

    else:

        print("Can not find a number at the end of string")

check('Kamalesh007')

check('Kamalesh')

4.Write a Python program to search the numbers (0-9) of length between 1 to 3 in a given string

import re

str = "587t3828gi988ey98y12y8ye9y32993"

check = re.findall('[0-9]{1,3}', str)

print(check)

5.Write a Python program to match a string that contains only uppercase letters.

import re

def check(str):

    if re.match('^[A-Z]*$', str):

        print("Found uppercase letters in the string")

    else:

        print("No uppercase letters were found in the string")

check("HELLOTHERE")

check("hellothere")


