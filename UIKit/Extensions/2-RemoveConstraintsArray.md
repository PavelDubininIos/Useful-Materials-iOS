# Remove constraints with Array

```swift
extension Array {
    
    func removeConstraints() {
        self.forEach {
            ($0 as? UIView)?.translatesAutoresizingMaskIntoConstraints = false
        }
    }
}
```

## Example
```swift
    override func viewDidLoad() {
        super.viewDidLoad()
        ...
        viewTranslatesAutoresizingMaskIntoConstraints()
        ...
    }
    
    private func viewTranslatesAutoresizingMaskIntoConstraints() {
        [firstView, secondView].removeConstraints()
    }

```
