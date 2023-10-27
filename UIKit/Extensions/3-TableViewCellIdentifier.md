# Table View Cell Identifier

```swift
extension UITableViewCell {
    
    static var identifier: String {
        return String(describing: Self.self)
    }
}
```

## Example
```swift
func tableView(_ tableView: UITableView, cellForRowAt indexPath: IndexPath) -> UITableViewCell {
    let cell = tableView.dequeueReusableCell(withIdentifier: ExampleScreenCell.identifier, for: indexPath) as! ExampleScreenCell
    ...
    return cell
```
```swift
override func viewDidLoad() {
    ...
    tableView.register(ExampleScreenCell.self, forCellReuseIdentifier: ExampleScreenCell.identifier)
    ...
}
```
