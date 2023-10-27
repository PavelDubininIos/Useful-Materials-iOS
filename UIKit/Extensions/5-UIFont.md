# UIFont Extension

```swift
extension UIFont {
    static func helvetica16() -> UIFont? {
        return UIFont.init(name: "Helvetica", size: 16)
    }
    
    static func helvetica24Bold() -> UIFont? {
        return UIFont.init(name: "Helvetica-Bold", size: 24)
    }
    
    static func helvetica16Bold() -> UIFont? {
        return UIFont.init(name: "Helvetica-Bold", size: 16)
    }
}
```

## Example
```
    private lazy var SomeLabel: UILabel = {
        let label = UILabel()
        label.font = .helvetica16()
        ...
        return label
    }()
```
