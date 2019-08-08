// An array is an ordered set of values of the same type
var numbers = [4, 8, 12, 18, 7, -1, 86]


var number: [Int] = [4, 8, 12, 18, 7, -1, 86]

var names = ["pim", "pam", "poum"] 

names.insert("toto", at: 1)
names.remove(at: 0)
names

// Search for an item
names.index(of: "toto")

if names.index(of: "titi") != nil {
    print("il est dans le tableau")
} else {
    print("il n'est pas dans le tableau")
}

for name in names {
    print(name)
}

for index in 0..<names.count {
    print("\(index) : names[index])")
}

for (index, name) in names.enumerated() {
    print("\(index) : \(names[index])")
}

var shoppingList = [String]()
shoppingList.append("bread")
shoppingList.append("water")

shoppingList[0]
shoppingList[1]

// ShoppingList[2]
shoppingList[0] = "beer"

shoppingList.append("paper")
shoppingList

shoppingList.count
shoppingList.isEmpty

for shopping in shoppingList {
print(shopping)
}
