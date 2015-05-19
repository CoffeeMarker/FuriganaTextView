# FuriganaTextView
A simple wrapper view for UITextView that can display Furiganas.

![Example](https://raw.githubusercontent.com/Liulishuo-iOS/FuriganaTextView/master/img/example.png)

### How to Use
```swift

// Prepare furigana contents
let furiganas = [
  Furigana(text: "た", original: "田", range: NSMakeRange(0, 1)),
  Furigana(text: "なか", original: "中", range: NSMakeRange(1, 1)),
]
let contents = NSAttributedString(string: "田中さん、中華料理を食べたことありますか。")

// Tell FuriganaTextView about 
// the furiganas (which is an array of the Furigana struct) 
// and the contents to display (a NSAttributedString)
furiganaTextView.furiganas = furiganas
furiganaTextView.contents = contents

```

For more configurable properties, see `/src/FuriganaTextView.swift`.

### Building and Deployment Target

* Builds with __Xcode 6.3__ and __Swift 1.2__
* Supports __iOS 7 and above__

### Known Issues
* The `textContainerInset` property of the wrapped `UITextView` seems not working correctly.
* Furiganas displayed in vertical writing is not implemented yet.
