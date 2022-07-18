## Hello World

```swift
import Love
import Happiness
import HwFamily
let 🦀 = HwBaby(
    fullName: "Nguyễn Hữu Hoàng Nam",
    gender: Gender.Male,
)
🦀.helloWorld()

```

<details>
    <summary>Runnable swift code here</summary>
    
```swift
import Foundation
enum Gender{
    case Male
    case Female
}
class Person{
    let dob: Date
    let gender: Gender
    private(set) var givenName: String
    private(set) var familyName: String
    init(givenName: String,
         familyName: String,
         dob: Date,
         gender: Gender){
        self.givenName = givenName
        self.familyName = familyName
        self.dob = dob
        self.gender = gender
    }
    var fullName: String{
        get {
            return "\(self.familyName) \(self.givenName)"
        }
    }
}
class Hw: Person{
    let hwFamilyName = "Nguyễn"
    init(name: String, dob: Date, gender: Gender) {
        super.init(givenName: name,
                   familyName: hwFamilyName,
                   dob: dob,
                   gender: gender)
    }
}
protocol Linz{
}
class HwBaby: Hw, Linz{
    public func helloWorld(){
        print("Oe! Oe! Oe!")
    }
}

let 🦀 = HwBaby(
    name: "Hữu Hoàng Nam",
    gender: Gender.Male
)
print("Name: \(🦀.fullName)")
🦀.helloWorld()

``` 
</details>

## Happy Cua
![Cua's Smile](img/CuaSmiling.JPG)
