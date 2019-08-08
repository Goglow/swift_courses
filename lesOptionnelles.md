
/* The variables of the "optional" type have:
- a value
- no value -> nil
 
Many functions or APIs return an "optional" to handle the case where they can not return a value */

let oneNumber = Int("18")

let oneOtherNumber = Int("dixhuit")

let myImage = UIImage(named: "image_name")

// Forced unwrap
let toto = oneNumber! + 2

if oneNumber != nil {
    let toto = oneNumber! + 2
    toto
    print("la valeur est \(oneNumber!)")
} else {
    print("no value for toto")
}

var myOptional: Int? = 7
myOptional = nil
myOptional = 8

// Optional binding
if let number = Int("18") {
    print(number)
} else {
    print("conversion to failure")
}

if let myImage = UIImage(named: "image_name") {
    print(myImage)
}

// At the output of a function
func squareRootOne(_ x: Double) -> Double {
    return sqrt(x)
}

squareRootOne(10)

func squareRootTwo(_ x: Double) -> Double? {
    if x > 0 {
    return sqrt(x)
} else {
    return nil
    }
}

squareRootTwo(-2)
