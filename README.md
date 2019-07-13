# Functions lab 1

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.


## Question 1

Complete the function so that it will print out total cost after tax. Make sure to **call the function** afterwards.

```swift
let itemCost = 45.0
let nyTax = 0.08775

func totalWithTax() {
    let tax = (itemCost * nyTax)
    let total = (itemCost + tax)
    print(total)
}
totalWithTax()
```

Then, modify the function you implemented to have a return type of `Int`, and use an external name that looks more readable. Function calls should look something like "total cost of the item after tax"

## Question 2

Convert the the following if/else statement below into function with a `String` return type.

```swift
let todaysTemperature = 72

if todaysTemperature <= 40 {
    print("It's cold out.")
} else if todaysTemperature >= 85 {
    print("It's really warm.")
} else {
    print("Weather is moderate.")
}
```

```swift
func HowIsTheWeather (t: Int) -> String {
    var temp = ""
    if t <= 40 {
        temp = "It's cold out."
    } else if t <= 85 {
        temp = "It's really warm."
    } else {
        temp = "Weather is moderate."
    }
    return temp
}
print(HowIsTheWeather(t: 72))
```


## Question 3

Write a function named `min2` that takes two `Int` values, `a` and `b`, and returns the smallest one.

Function Definition
`func min2(a: Int, b: Int) -> Int`

Example:
Input: `min2(a:1, b:2)`

Output: `1`

```swift
func min2(a: Int, b: Int) -> Int {
    var min = 0
    if a < b {
        min = a
    } else if a > b {
        min = b
    }
    return min
}
print(min2(a: 1, b: 2))
```


## Question 4

Write a function that takes an `Int` and returns its last digit. Name the function `lastDigit`. Use _ to ignore the external parameter name.

Function Definition:
`func lastDigit(_ number: Int) -> Int`

Example:
Input: `lastDigit(12345)`

Output: `5`

```swift
func lastDigit(_ number: Int) -> Int {
    let last = (number % 10)
    return last
}
print(lastDigit(12345))
```

## Question 5

Write a function that takes in any two positive integers and return the sum.

```swift
func sum2(a: Int, b: Int) -> Int {
    var sum = 0
    if a > 0 && b > 0 {
        sum = (a+b)
    }
return sum
}
print(sum2(a: 10, b: 2))
//prints 0 if any int is negative. refactor this!
```


## Question 6

Write a function takes in any number grade and returns a corresponding letter grade.

| Number Grade | Equivalent Letter Grade |
| :--------: | :---------: |
| 100 | A+ |
| 90 - 99 | A |
| 80 - 89 | B |
| 70 - 79 | C |
| 65 - 69 | D |
| Below 65 | F |

```swift

func gradeConverter(_ number: Int) -> String {
var grade = ""
    if number == 100 {
        grade = "A+"
    } else if number >= 90 && number <= 99 {
        grade = "A"
    } else if number >= 80 && number <= 89 {
        grade = "B"
    } else if number >= 70 && number <= 79 {
        grade = "C"
    } else if number >= 65 && number <= 69 {
        grade = "D"
    } else {
        grade = "F"
    }
return grade
}
print(gradeConverter(65))
```

## Question 7

Make a calculator function that takes in three parameters (two numbers and one operator) and returns the answer of the operation.

Operator parameter: (+, -, x, /)

```swift
func calculator(a: Int, b: Int, o: Character) -> Int {
    var result = 0
    if o == "+" {
        result = a + b
    } else if o == "-" {
        result = a - b
    } else if o == "x" {
        result = a * b
    } else if o == "/" {
        result = a / b
    }
    return result
}
print(calculator(a: 10, b: 2, o: "/"))
```


## Question 8

Write a function so that it will print out **total cost after tip.**

```swift
let mealCost = 45
let tipPercentage = 0.15

func totalWithTip() -> Int {
    let tip = (Double(mealCost) * tipPercentage)
    let total = (Double(mealCost) + tip)
    return Int(Double(total))
}
let myFinalCost = totalWithTip() //Fill in the arguments
print(myFinalCost)
```

Write a function that will print out **total cost after tip and tax.**

```swift
let taxPercentage = 0.09

func totalWithTipAndTax() -> Int {
    let tip = (Double(mealCost) * tipPercentage)
    let tax = (Double(mealCost) * taxPercentage)
    let total = (Double(mealCost) + tip + tax)
    return Int(Double(total))
}

let myFinalCostWithTipAndTax = totalWithTipAndTax()
print(myFinalCostWithTipAndTax)
```


## Question 9

Implement a function named `repeatPrint` that takes a string `message` and a integer `count` as parameters. The function should print `message` `count` number of times and then print a newline.

Example:
Input: `repeatPrint(message: "+", count: 10)`

Output: `++++++++++`

```swift
func repeatPrint(message: String, n: Int) -> Void {
    for _ in 0..<n{
        print(message)
    }
}
repeatPrint(message: "I'm tired.", n: 10)
```


## Question 10

Write a function named `first` that takes an Int named n and returns an array with the first n numbers starting from 1.

Function Definition
`func first(_ n: Int) -> [Int]`

Example:
Input: `first(3)`

Output: `[1, 2, 3]`

```swift
func first(_ n: Int) -> [Int] {
    return Array(1...n)
}
print(first(10))
```


## Question 11

Write a function that prints the numbers from 1 to x, except:

If the number if a multiple of 3, print `"Fizz"` instead of the number
If the number is a multiple of 5, print `"Buzz"` instead of the number
If the number is a multiple of 3 AND 5, print `"FizzBuzz"` instead of the number
Your function should take in one parameter: x (the number to count up to)


## Question 12

Write a function named `reverse` that takes an array of integers named `numbers` as a parameter. The function should return an array with the numbers from `numbers` in reverse order.


Example:
Input: `reverse([1, 2, 3])`

Output: `[3, 2, 1]`

```swift
var arrayInput = [1, 2, 3]

func reverse(array: [Int]) -> [Int] {
    return arrayInput.reversed()
}
print(reverse(array: arrayInput))
```


## Question 13

Write a function that prints out the most frequently appearing Int in an array of Int.

```swift
var someRepeatsAgain = [1,2,3,5,3,5,8,4,7,2,4,8,8,5,6,5,5]
func repeatsIdentifier (array: [Int]) -> Int {
    var freqDict = [Int: Int]()
    for num in array {
        if freqDict.keys.contains(num) {
            freqDict[num] = freqDict[num]! + 1
        } else {
            freqDict[num] = 1
        }
    }
    var resultTuple:(Int,Int) = (0,0) // Using a tuple to store the most repeated key and its value
    for (key, value) in freqDict {
        if value > resultTuple.1 { // Compare with the value with the tuple value
            resultTuple = (key, value)
        }
    }
    return resultTuple.0 // Return tuple key
}
print(repeatsIdentifier(array: someRepeatsAgain))
```


## Question 14

Write a function that sums all the even indices of an array of Ints.

```swift
var arrayOfInts = [2, 2]

func sumOfInts (array: [Int]) -> Int {
    var evenNumbers: [Int] = []
    for num in array {
        if num % 2 == 0 {
            evenNumbers.append(num)
        }
    }
    var sumOfInts = 0
    for num in evenNumbers {
        sumOfInts = sumOfInts + num
    }
    return sumOfInts
}

print(sumOfInts(array: arrayOfInts))

```


## Question 15

Write a function that flips a dictionary.  All of the keys are now values and all of the values are now keys.

Example:
Input: `[1: "hi", 5: "bye:]`

Output: `["hi": 1, "bye": 5]`

```swift
let inputDic = [1: "hi", 5:"bye"]

func flipper(dictionary: [Int:String]) -> [String:Int] {
    var flippedDictionary: [String:Int] = [:]
    for (key, value) in dictionary {
        flippedDictionary[value] = key
    }
    return flippedDictionary
}
print(inputDic)
```


## Question 16

Write a function that finds the person with the second highest test score in a Dictionary that maps names to scores.

Example:
Input: `["Person 1": 83, "Person 2": 74, "Person 3": 82]`

Output: `"Person 3"`

```swift
func highest(dicNames: [String:Int]) -> String {
    var highestScore = 0
        for (_, value) in dicNames {
            if value > highestScore {
                highestScore = value
            }
    }
    var secondPerson = ""
    for (key, value) in dicNames {
        if value < highestScore && value != highestScore {
            secondPerson = key
        }
    }
    return secondPerson
}
print(highest(dicNames: scores))
```

## Question 17

Write a function that determines if a value is inside of array.
```swift
let arrayInput =  ["Eliel", "Mariel", "Mariangel", "Sophia","Mushroom"]
var valueInput = "Mariel"

func inside(array: [String], value: (String)) -> Bool {
    return(array.contains(value))
}
print(inside(array: arrayInput, value: "Mariel"))
```

## Question 18

Write a function takes an `Int` as input, and returns true if it is even, or false if it is odd.
Using your new function, write code that prints out whether `dieRoll` is even or odd:

`let dieRoll = Int(arc4random_uniform(6) + 1)`

```swift
func evenOrOdd(number: Int) {
    if number % 2 == 0 {
        print("Number is even.")
    } else {
        print("Number is odd.")
    }
}
evenOrOdd(number: dieRoll)
```


## Question 19

Write a function that takes `[Int]` as input. It should return the largest Int in the array.

Using your function from the first step, use String interpolation to print a sentence that states what the largest Int in `myArray` is.

`let myArray = [3,5,1,3,532,1,4,91,20,30,92,143]`

```swift

func largestNumber(array: [Int]) {
    var largest = 0
    for n in array {
        if n > largest {
            largest = n
        }
    }
    print("The largest number in array is \(largest).")
}
largestNumber(array: myArray)
```

If you haven't already done so, write a function that takes in an Int and returns whether that number is even or odd. Use that function to print a sentence that states whether the largest Int in `myArray` is even or odd.

```swift
func evenOrOdd(number: Int) {
    if number % 2 == 0 {
        print("\(number) is an even number.")
    } else {
        print("\(number) is an odd number.")
    }
}
evenOrOdd(number: 532)

```

## Question 20

Write a function that takes a String as input and returns the number of characters in the string

Using your function, print how many characters are in myString:

`let myString = "Swift is a new programming language for iOS, OS X, watchOS, and tvOS apps that builds on the best of C and Objective-C, without the constraints of C compatibility."`

```swift
func characterCounter(inputString: String) {
    var counter = 0
    for c in inputString where c != " " {
        counter += 1
        }
    print(counter)
}
characterCounter(inputString: myString)
```


## Question 21

Write a function that counts how many characters in a String match a specific character.  (e.g: count how many "a"s are in a String, or count how many ","s are in a String.

Example:
Input:
```swift
let testString = "This is a test string for your code"
let targetCharacter: Character = "i"
```
```swift
func characterCounter(stringInput: String, characterInput: Character) -> Int {
    var freqC = [Character: Int]()

    for c in stringInput {
        if freqC.keys.contains(c) {
            freqC[c] = freqC[c]! + 1
        } else {
            freqC[c] = 1
        }
    }
    return freqC[characterInput] ?? 0
}
print(characterCounter(stringInput: testString, characterInput: targetCharacter))
```

Sample output: `3`


## Question 22

Write a function that counts how many characters in a String match one of several possible characters.  (e.g: count how many vowels are in a String, or count how many "a"s "b"s and "c"s are in a Sting)

Example:
Input:
```swift
let inputString = "This one is a little more complicated"
let targetCharacters: [Character] = ["a","e","i","o","u"]
```

Output: `13`

```swift
func characterCounter(stringInput: String, characterInput: [Character]) -> Int {
    var freqC = [Character: Int]()

    for c in stringInput {
        if freqC.keys.contains(c) {
            freqC[c] = freqC[c]! + 1 //if key is found add one to the value.
        } else {
            freqC[c] = 1 //initialize an entry in my frequency dictionary with the value 1.
        }
    }

    var totalCharacters = 0
    for (key, value) in freqC { //for each key value pair in dictionary ...
        if  characterInput.contains(key) { //if character array contains the key...
            totalCharacters += value //add the value of the key to the counter
        }
    }
    return totalCharacters  //returns the sum of all appearances of characters in character input.
    }
print(characterCounter(stringInput: inputString, characterInput: targetCharacters))
```


## Question 23

Write a function that returns the number of unique Ints in an array of Ints.

Example:
Input: `let inputArray2 = [3,1,4,1,3,2,6,1,9]`

Output: `4`

//Explanation: 2, 4, 6, 9 are unique in the array. Every other number is not unique.

```swift
let inputArray2 = [3,1,4,1,3,2,6,1,9]
func unique(array: [Int]) -> [Int] {
    var resultArray: [Int] = []
    var dictionary: [Int:Int] = [:]
    for n in array {
        if dictionary.keys.contains(n) {
            dictionary[n] = dictionary[n]! + 1 //if key is found add one to the value.
        } else {
            dictionary[n] = 1 //initialize an entry in my frequency dictionary with the value 1.
        }
    }
    for (key, value) in dictionary where value == 1 {
        resultArray.append(key)
    }
    return resultArray
}
print(unique(array: inputArray2))
```


## Question 24

Write a function that converts a binary number into decimal. The binary number will be given as an array of Ints.

Example:
Input: `let binaryArray = [1,0,1,1,1,0,1]`

Output: `93`

```swift
let binaryArray = [1,0,1,1,1,0,1]

func binaryToDecimal(array:[Int]) -> Int {
    var decimal = 0
    for (i, n) in array.reversed().enumerated() { // i = index, n = index value.
        decimal += (n * Int(pow(Double(2), Double(i))))
        //decimal = previous value of decimal + number * 2^i 
    }
    return decimal
}
print(binaryToDecimal(array: binaryArray))
```

## Question 25

Write a function named `timeDifference`. It takes as input four numbers that represent two times in a day and returns the difference in minutes between them. The first two parameters `firstHour` and `firstMinute` represent the hour and minute of the first time. The last two `secondHour` and `secondMinute` represent the hour and minute of the second time. All parameters should have external parameter names with the same name as the local ones.

Example:
Input: `timeDifference(firstHour: 12, firstMinute: 3, secondHour: 13, secondMinute: 10)`

Output: `67`

```swift
var firstHour = 12
var firstMinute = 3
var secondHour = 13
var secondMinute = 10

func timeDifference(firstHour: Int, firstMinute: Int, secondHour: Int, secondMinute: Int) -> Int {
    let differenceHours = (secondHour - firstHour) * 60
    let differenceMinutes = (secondMinute - firstMinute)

    return (differenceHours + differenceMinutes)
}
print(timeDifference(firstHour: firstHour, firstMinute: firstMinute, secondHour: secondHour, secondMinute: secondMinute))
```


## Question 26

Write a function called `filterOdd` that takes an array of ints and returns it with just the even numbers.

Example:
Input:  `filterOdd(arr: [1, 2, 3, 4, 5, 6, 7, 8])`

Output: `[2, 4, 6, 8]`

```swift
func filterOdd(array: [Int]) -> [Int] {
var filtered: [Int] = []
    for n in array {
        if n % 2 == 0 {
            filtered.append(n)
        }
    }
    return filtered.sorted()
}
print(filterOdd(array: arr))
```


## Question 27

Write a function called `doubleIt` that takes an array of ints and returns it with all the elements doubled.

Example:
Input: `doubleIt(arr: [1, 2, 3, 4])`

Output: `[2, 4, 6, 8]`

```swift
func doubleIt(array: [Int]) -> [Int] {
    var doubles: [Int] = []
    var nTimes2 = 0
    for number in array {
        nTimes2 = (number * 2)
        doubles.append(nTimes2)
        nTimes2 = 0
    }
    return doubles
}
print(doubleIt(array: arr))
```


Then write a function called `multiplyBy` that takes an array of ints and an int n that will return the array with all the elements multiplied by n.

Example:
Input:  `multiplyIt(arr: [1, 2, 3, 4], n: 4)`

Output:  `[4, 8, 12, 16]`

```swift
func multiplyIt(array: [Int], number: Int) -> [Int] {
    var result: [Int] = []
    var timesN = 0
    for n in array {
        timesN = (n * number)
        result.append(timesN)
        timesN = 0
    }
    return result
}
print(multiplyIt(array: arr, number: 4))
```



## Question 28

Write a function called `unwrap` that takes an array of optional ints and returns an array with them unwrapped with any nil values removed.

Example:
Input:  `unwrap(arr: [nil, 7, 4, nil, 43, 11, nil, 2])`

Output: `[7, 4, 43, 11, 2]`
```swift
func unwrap(array: [Int?]) -> [Int] {
    var result:[Int] = []
    for number in array {
        if let unwrapNumber = number {
            result.append(unwrapNumber)
        }
    }
    return result
}
print(unwrap(array: arr))
```


## Question 29

Write a function that takes an array of bools and returns a dictionary that maps the bools to how many times they appear in the array.

Example:
Input:  `countBools(arr: [true, true, false, true, false, true])`

Output: `[false: 2, true: 4]`

```swift
let arr = [true, true, false, true, false, true]
func countBools(array: [Bool]) -> [Bool:Int] {
    var dictionary: [Bool:Int] = [:]

    for i in array {
        if dictionary.keys.contains(i) {
            dictionary[i] = dictionary[i]! + 1
        } else {
            dictionary[i] = 1
        }
    }

    return dictionary
}
print(countBools(array: arr))
```


## Question 30

Write a function that takes a string as input and returns a dictionary that maps each unique character to how many times they appear in the string.

Example:
Input:  `countCharacters(str: "Hello, World!")`

Output: `["H": 1, "r": 1, "!": 1, "e": 1, "o": 2, "l": 3, ",": 1, " ": 1, "W": 1, "d": 1]`

```swift
let str = "Hello, World!"
func characterCounter(stringInput: String) -> [Character:Int] {
    var freqC = [Character: Int]()

    for c in stringInput {
        if freqC.keys.contains(c) {
            freqC[c] = freqC[c]! + 1 //if key is found add one to the value.
        } else {
            freqC[c] = 1
        }
    }

    return freqC
}
print(characterCounter(stringInput: str))

```
## Question 31

Write a function that takes this dictionary of baseball teams by ID and returns an array of tuples that contain each team's ID and name.

`let baseballTeamsById = [1001:"Mets", 1002:"Yankees", 1003:"Rays", 1004:"Marlins"]`

Example:
Input:  `dictToTuples(dict: baseballTeamsById)`

Output: `[(.0 1003, .1 "Rays"), (.0 1001, .1 "Mets"), (.0 1004, .1 "Marlins"), (.0 1002, .1 "Yankees")]`


## Question 32

Write a function that checks if a String is a [Palindrome](https://en.wikipedia.org/wiki/Palindrome)


## Question 33

Write a function that checks if a String is a [pangram](https://en.wikipedia.org/wiki/Pangram)


## Question 34

Write your own `min()` and `max()` functions for an Array of Ints


## Question 35

Given two arrays of Ints, write a function that tells you all the values they have in common.


## Question 36

Find the most-frequently appearing Array of Ints in an Array of Arrays of Ints.


## Question 37

Given a String as input, rotate all a-z characters by one.  This is called [ROT-1 encryption](http://www.rot-n.com/).

Sample input:
`This is a test string. Anything can be written in here (even Zebras and zebras).`

Sample output:
`Uijt jt b uftu tusjoh. Bozuijoh dbo cf xsjuufo jo ifsf (fwfo Afcsbt boe afcsbt).`
