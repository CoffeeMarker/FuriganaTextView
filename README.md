# FuriganaTextView
A simple wrapper view for UITextView that can display Furiganas.

### How to Use
```swift

// Prepare furigana contents
let furiganas = [
  Furigana(text: "た", original: "田", range: NSMakeRange(0, 1)),
  Furigana(text: "なか", original: "中", range: NSMakeRange(1, 1)),
]
let contents = NSAttributedString(string: "田中さん、中華料理を食べたことありますか。")

// Tell FuriganaTextView about the furiganas(an array of Furigana struct) 
// and the contents to display(a NSAttributedString)
furiganaTextView.furiganas = furiganas
furiganaTextView.contents = contents

```

For more configurable properties, see `/src/FuriganaTextView.swift`.

### Known Issues
* The `textContainerInset` property of the wrapped `UITextView` seems not working correctly.
* Furiganas displayed in vertical writing is not implemented yet.
