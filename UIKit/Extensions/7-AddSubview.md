# Add Subview

```swift
extension UIView {
    
    func addSubviews(_ subviews: UIView...) {
        subviews.forEach { addSubview($0) }
    }
    
    func makeShadowUnderView() {
        layer.shadowRadius = 10.0
        layer.shadowOpacity = 0.1
        layer.masksToBounds = false
        layer.shadowColor = UIColor.black.cgColor
        layer.shadowOffset = CGSize(width: 3.0, height: 3.0)
    }
}
```

## Example
```swift
    private func setupViews() {
        topView.addSubviews(someImage, anotherImage, someLabel)
        
        NSLayoutConstraint.activate([
        ...
        ])
    }
```
