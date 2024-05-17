Check if The Two Strings are Anagram or not
Anagram program in python is when strings share the same no of characters and also the same characters then strings are called anagrams. The rearrangement of similar characters or letters in a string even if they don’t have the same meanings are anagrams. Only one strict rule is followed if we create anagrams of a string ‘count of every character available in the 1st string should be equal to the count of characters in the 2nd string for the same character.

Python program to check if two Strings are Anagram or not
Anagram Program in Python
Two strings S1 and S2 are anagrams of one another if –

By re-arranging characters of string1 (s1) we can form string2 (s2) and vice versa

Python program to check if two Strings are Anagram or not
Check if two Strings are Anagram or not in Python
Algorithm
Method 1: Sorts both string and check if the results are same or not
Method 2: Uses counter method that gives results of individual counts of items present in the list, and compare them
Method 1
This method first converts both strings into lowercase
We sort both of the strings
We then compare both resultant strings
If they are same then they must be anagrams
# Anagram program in python
# take user input
String1 = "Listen"
String2 = "Silent"

String1 = sorted(String1.lower())
String2 = sorted(String2.lower())

print("String1 after sorting: ", String1)
print("String2 after sorting: ", String2)

# check if now strings matches
if String1 == String2:
    print('Strings are anagram')
else:
    print('Strings are not anagram')
Output:
String1 after sorting:  ['e', 'i', 'l', 'n', 's', 't']
String2 after sorting:  ['e', 'i', 'l', 'n', 's', 't']
Strings are anagram
Method 2
We use counter method from the collections library for this.

The counter method can be used as –

For string: Listen
Counter(string)
printing this counter string will give a result –

Counter({'l': 1, 'i': 1, 's': 1, 't': 1, 'e': 1, 'n': 1})
We can then compare both counters for both the strings.

# Check if two Strings are Anagram or not in Python
from collections import Counter


def check(s1, s2):
    # printing counter
    print(Counter(s1))
    print(Counter(s2))
    # implementing counter function
    if Counter(s1) == Counter(s2):
        print("The strings are anagrams.")
    else:
        print("The strings aren't anagrams.")


# driver code
s1 = "Listen"
s2 = "silent"
check(s1.lower(), s2.lower())
Output:
Counter({'l': 1, 'i': 1, 's': 1, 't': 1, 'e': 1, 'n': 1})
Counter({'s': 1, 'i': 1, 'l': 1, 'e': 1, 'n': 1, 't': 1})
The strings are anagrams.
