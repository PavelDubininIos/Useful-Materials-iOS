# Stack View Extension

```swift
extension UIStackView {
    
    convenience init(arrangedSubviews: [UIView], axis: NSLayoutConstraint.Axis, spacing: CGFloat) {
        self.init(arrangedSubviews: arrangedSubviews)
        self.axis = axis
        self.spacing = spacing
        self.translatesAutoresizingMaskIntoConstraints = false
    }
    
    convenience init(_ axis: NSLayoutConstraint.Axis,
                               _ distribution:UIStackView.Distribution,
                               _ alignment: UIStackView.Alignment,
                               _ spacing: CGFloat,
                               _ arrangedSubviews: [UIView] ) {
            self.init(arrangedSubviews: arrangedSubviews)
            self.axis = axis
            self.distribution = distribution
            self.alignment = alignment
            self.spacing = spacing
            self.backgroundColor = .clear
        }
}
```

## Example
```swift
    private var fullStackView = UIStackView()
    
    private func viewTranslatesAutoresizingMaskIntoConstraintsToFalse() {
        [
            ...
            fullStackView,
            ...
        ]
            .removeConstraints()
    }
    
    private func configStacks() {
        ...
        fullStackView = UIStackView(.vertical, .fill, .fill, 0, [topView, bottomView])
        ...
    }    
    
    private func setupViews() {
        visibleView.addSubview(fullStackView)
        ...
        
            NSLayoutConstraint.activate([
            
            fullStackView.topAnchor.constraint(equalTo: visibleView.topAnchor),
            fullStackView.leadingAnchor.constraint(equalTo: visibleView.leadingAnchor),
            fullStackView.trailingAnchor.constraint(equalTo: visibleView.trailingAnchor),
            fullStackView.bottomAnchor.constraint(equalTo: visibleView.bottomAnchor),
            ...
            ])
            
    }
```
