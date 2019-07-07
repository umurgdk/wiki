# Apple tvOS Notes

## UITableView

UITableView has safe are insets by default. That makes the cells have 90pt margins on both sides. To remove this artefact:

```swift
tableView.insetsContentViewsToSafeArea = false
tableView.insetsLayoutMarginsFromSafeArea = false
```

- [Focus engine quirks](/programming/tvos/focus_engine)
