## Hello World

```swift
import Love
import Happiness
import HwFamily
let 🦀 = HwBaby(
    fullName: "Nguyễn Hữu Hoàng Nam",
    gender: Gender.Male,
    dob: Date("29/06/2021")
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
extension Date{
    static var formatter: DateFormatter{
        get {
            let formatter = DateFormatter()
            formatter.dateFormat = "dd/MM/yyyy hh:mm"
            formatter.timeZone = TimeZone(identifier: "Asia/Ho_Chi_Minh")
            return formatter
        }
    }
    init(_ dateStr: String){
        self = Date.formatter.date(from: dateStr)!
    }
    func string() -> String {
        return Date.formatter.string(from: self)
    }
}
let 🦀 = HwBaby(
    name: "Hữu Hoàng Nam",
    dob: Date("29/06/2021 10:00"),
    gender: Gender.Male
)
print("Name: \(🦀.fullName))
print("Date of birth: \(🦀.dob.string()))
🦀.helloWorld()

``` 
</details>
