## Hello World

```swift
import Foundation
enum Gender{
    case Male
    case Female
}
class OurBaby{
    public let fullName: String
    public let dob: Date
    public let gender: Gender
    public init(fullName: String, gender: Gender, dob: Date){
        self.fullName = fullName
        self.dob = dob
        self.gender = gender
    }
    public func helloWorld(){
        print("Oe! Oe! Oe!")
    }
}
let formatter = DateFormatter()
formatter.dateFormat = "dd/MM/yyyy"
let cua = OurBaby(
    fullName: "Nguyễn Hữu Hoàng Nam",
    gender: Gender.Male,
    dob: formatter.date(from: "29/06/2021")!
)
cua.helloWorld()

```
