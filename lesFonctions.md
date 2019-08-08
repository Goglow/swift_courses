
// Functions with no argument or exit value
func myFirstFunction() {
    print("Hello World")
}

myFirstFunction()

// With an argument
func showMoreOne (x: Int) {
    print(x + 1)
}
showMoreOne(x: 8)

func moreOne (x: Int) -> Int {
    return x + 1
}
moreOne(x: 8)

func addInteger (x: Int, y: Int) -> Int {
    return x + y
}
addInteger(x: 7, y: 18)
