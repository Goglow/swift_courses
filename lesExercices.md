
// Exercise: Write a function that takes as parameters two integers and returns their sum

func sum(a: Int, b: Int)  -> Int {
    return a + b
}

sum(a: 4, b: 7)

let number1 = 18
let number2 = 21
sum(a: number1, b: number2)

// Exercise: Write a function that takes an integer parameter and displays that integer plus one in the console

func moreOne(x: Int) {
    print(x + 1)
}

moreOne(x: 7)

let number = 18
moreOne(x: number)


// Exercise: Write a function sayHello that takes a string parameter and returns this string preceded by the text "Hello"

func sayHello(name: String) -> String {
    return "Hello " + name
}

sayHello(name: "Waggle")

// Or

func sayBye(name: String) -> String {
    return "Bye \(name)"
}

sayBye(name: "Waggle")


// Exercise: Write a function that takes an integer parameter and which shows in the console "you are major" if this integer is greater than or equal to 18 and "you are minor" if not

func majority(age: Int) {
    if age >= 18 {
        print("You are major")
    } else {
        print("You are minor")
    }
}

majority(age: 15)
majority(age: 23)

// Return a boolean

func isMajor(age: Int) -> Bool {
    return age >= 18
}

isMajor(age: 14)


// Exercise : Write a function that takes as parameter a double table and returns the sum of its elements

func sumNumbers(numbers: [Double]) -> Double {
    var output = 0.0
    for number in numbers {
        output += number
    }
    return output
}

sumNumbers(numbers: [4, 5.0, 7])
let toto = [8.7, 7, 18]
sumNumbers(numbers: toto)
sumNumbers(numbers: [Double]())


// Exercise : Write a function that takes an array of Int as well as an integer and returns a table consisting of elements of the array larger than this integer

func getBiggerThan(minimum: Int, numbers: [Int]) -> [Int] {
    var output = [Int]()
    
    for number in numbers {
        if number > minimum {
            output.append(number)
        }
    }
    
    return output
}

getBiggerThan(minimum: 4, numbers: [5, 8, 2, 0, -1, 18])

func getBiggerThan(minimum: Int, fromArray numbers: [Int]) -> [Int] {
    var output = [Int]()
    
    for number in numbers {
        if number > minimum {
            output.append(number)
        }
    }
    
    return output
}

getBiggerThan(minimum: 4, fromArray: [5, 8, 2, 0, -1, 18])


// Exercise : Write a function that concatenates two arrays of integers, that is, returns a table composed of the elements of the first array, followed by the elements of the second array

func concateneArrayInt (array1: [Int], array2: [Int]) -> [Int] {
    var output = array1
    for number in array2 {
        output.append(number)
    }
    
    return output
}

let array1 = [2, 1, 4]
let array2 = [7, 18]

concateneArrayInt(array1: array1, array2: array2)

// Or

array1 + array2


func concateneArray<T> (array1: [T], array2: [T]) -> [T] {
    var output = array1
    for number in array2 {
        output.append(number)
    }
    
    return output
}

concateneArray(array1: ["pim", "pam"], array2: ["poum", "toto"])


// Exercise : Write a function that takes an array of integers as input and returns a table of even numbers from that array

let input = [4, 8, 7, 6, 18, -1, 47, 20, 12]
func selectEvenNumbers(numbers: [Int]) -> [Int] {
    var output = [Int]()
    
    for number in numbers {
        if number % 2 == 0 {
            output.append(number)
        }
    }
    
    return output
}

selectEvenNumbers(numbers: input)


// Exercise : Write a function that takes as input an array of strings and returns a dictionary that counts for each value of the array the number of times it appears

func countChaines (chaines: [String]) -> [String : Int] {
    var output = [String : Int]()
    
    for chaine in chaines {
        if output[chaine] != nil {
            output[chaine]! += 1
        } else {
            output[chaine] = 1
        }
    }
    return output
}

let input = ["pim", "pam", "poum", "pim", "toto", "pim"]
countChaines(chaines: input)


// Exercise : Write a function that takes an integer input and displays a triangle figure in the console as below with as many lines as the number in parameter
// For n = 3
// *
// **
// ***

func triangle(n: Int) {
    for index in 1...n {
        var ligne = ""
        for _ in 1...index {
            ligne += "*"
    
        }
        print(ligne)
    }
    
}
triangle(n: 3)

// A Christmas tree
// For n = 3
//   *
//  ***
// *****

func christmasTree(n: Int) {
    var position = n
    for index in 1...n {
        var ligne = ""
        for _ in 1..<position {
            ligne += " "
        }
        for _ in 1...(index * 2 - 1) {
            ligne += "*"
        }
        print(ligne)
        position -= 1
    }
    
}
christmasTree(n: 3)
