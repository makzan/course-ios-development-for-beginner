# Fetching JSON from Network

2 common ways:

- URLSession
- AlamoFire

----

# URLSession

----

- `URLSession` was renamed from `NSURLSession`
- Available since iOS 7
- Successor to `NSURLConnection`

----


# AlamoFire

- AlamoFire is 3rd party
- [Source code on github](https://github.com/Alamofire/Alamofire/)
- Latest stable version is 4.8.2
- Latest version is 5.0 beta 3.

----



# Managing 3rd party code

^We either use package manager or manual file import

1. Package Manager
2. File import

----

# Managing 3rd party code with package manager

- [Cocoapods](https://cocoapods.org)
- [Carthage](https://github.com/Carthage/Carthage)
- [Swift Package Manager](https://swift.org/package-manager/)

----

[Cocoapods vs Carthage vs Git Submodules](https://reallifeprogramming.com/carthage-vs-cocoapods-vs-git-submodules-9dc341ec6710)

----

# JSON to Swift

----

# Sample JSON

https://sample-json.netlify.com/macao-libraries.json

----

# Example of Codable Struct

```swift
struct Library: Codable {
    let name: String
    let open_hour: String
    let url: String
    let photo: String
    let lat: Double
    let lng: Double
}
```

----

```swift
struct Region: Codable {
    let region: String
    let libraries: [Library]
}
```

----

# Codable

- Convertible between JSON and Swift object
- If a property is present in JSON but not Swift, it will be ignored.
- If a property is present in Swift but not JSON, it must be optional.

----

# Difference between Class and Struct

1. No inheritance in Struct
2. Auto initializer in Struct
3. Struct is value type and Class is reference type

----

# AlamoFire Fetch Code Example

```swift
let urlString = "https://sample-json.netlify.com/macao-libraries.json"
Alamofire.request(urlString).validate().responseJSON { (response) in
    guard let data = response.data else {
        print("Fetch Error")
        return
    }
    guard let decodeResult = try? JSONDecoder().decode([Region].self, from: data) else {
        print("Decode error")
        return
    }
    self.result = decodeResult
}
```