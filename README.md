# Strings Lab 2

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.

## Question 1

You are given a string stored in variable `problem`. Write code so that you print each word of the string on a new line.

```swift
var problem = "split this string into words and print them on separate lines"
var word = ""
var array = [String] ()
for a in problem{
if a == " "{
array.append(word)
word = ""
continue
}
word += String(a)
}
array.append(word)
for a in array{
print(a)
print("")
}

```

Example

Input:
`var problem ="split this string into words and print them on separate lines"`

Output:
```swift
split
this
string
into
words
and
print
them
on
separate
lines
```


## Question 2

Given a string `testString` create a new variable called `condensedString` that has any consecutive spaces in `testString` replaced with a single space.

```swift
var problem = "  How   about      these spaces  ?  "
var word = ""
var array = problem.components(separatedBy: .whitespacesAndNewlines)
array.append(word)
for b in array where b != "" {
if b != " " {
word += b
word += " "
}
}
print(word)
```


## Question 3

Given a string with multiple words. Reverse the string word by word.

Example:

Sample Input: `"Swift is the best language"`

Sample Output: `"language best the is Swift"`
```swift
let problem = "Swift is the best language"
var word = ""
var minus = 0
var array = [String] ()
var newWord = ""
for a in problem{
if a == " "{
array.append(word)
word = ""
continue
}
word += String(a)
}
array.append(word)

minus = array.count-1

for _ in array{
newWord += array[minus] + " "
minus  -= 1

}
print(newWord)

```
## Question 4

Given a string with multiple words. Write code that prints how many of them are palindromes.

Example:

Sample Input: `"danaerys dad cat civic bottle"`

Sample Output: `2`
```swift
var problem = "danaerys dad cat civic bottle"
var reverString = ""
var word = ""
var trueCounter = 0
var array = [String] ()
for a in problem{
if a == " "{
array.append(word)
word = ""
continue
}
word += String(a)
}
array.append(word)
for b in array {
reverString = String(b.reversed())
if b == reverString{
trueCounter += 1
}
}
print(trueCounter)
```

## Question 5

You are given a string representing an **attendance record** for a student. The record only contains the following three characters:

`'A' : Absent.`

`'L' : Late.`

`'P' : Present.`

If a student has more than one 'A' or more than 2 continuous 'L's that student should not be rewarded. Print true if student is to be rewarded and False if they shouldn't.

Example:

Sample Input: `"PPALLP"`

Sample Output: `true`
```swift
var sampleInput = "PPALLP"
var A = 0
for a in sampleInput {
if a == "A" {
A += 1
}
}
if A > 1{
print(false)
} else if sampleInput.contains("LLL") {
print (false)
}else {
print(true)
}

```


## Question 6

Given a tuple with two strings. The first string is a **ransom note**, the second string being the characters from a magazine. Determine whether or not you can construct the ransom note using the characters from the magazine.

Each letter from the magazine can only be used once. You can assume all letters are lowercased.

Examples:
 

 

