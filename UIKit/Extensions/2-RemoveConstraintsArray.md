# Remove constraints with Array

```
extension Array {
    
    func removeConstraints() {
        self.forEach {
            ($0 as? UIView)?.translatesAutoresizingMaskIntoConstraints = false
        }
    }
}
```

## Example
```
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
