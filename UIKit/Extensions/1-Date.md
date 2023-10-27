# Date formate


## Date -> String
```swift
    extension Date {
    
    func toStringFormate(_ formateTo: String) -> String {
        let dateFormatter = DateFormatter()
        dateFormatter.dateFormat = formateTo
        return dateFormatter.string(from: self)
    }    
}
```

## String -> Date
```swift
extension String {
    
    func toStringDate(_ date: String) -> Date {
        let dateFormatter = DateFormatter()
        dateFormatter.dateFormat = "MMM d, yyyy"
        return dateFormatter.date(from: date) ?? Date()
    }
}
```
