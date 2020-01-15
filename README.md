# A [SwiftGen](https://github.com/SwiftGen/SwiftGen) SwiftUI template for Asset Catalogs

This template is a fork of [SwiftGen's bundled `xcassets/swift4.stencil` template](https://github.com/SwiftGen/SwiftGen/blob/master/templates/xcassets/swift4.stencil), to generate SwiftUI supporting type-safe code for colors and images in an Xcode asset catalog (`*.xcassets`).

It supports most of the same options, and produces mostly the same output.

🔥 Removed:
* Compiler checks for platform, as SwiftUI supports all Apple platforms
* Generation for data assets (including the `dataType` option parameter), as this template focuses on SwiftUI support
* Option parameters `colorAliasName`, and `imageAliasName`, as SwiftUI uses `Color` and `Image` types on all platforms

## Usage Example
```swift
// You can create new images with the convenience constructor like this:
let bananaImage = Image(Asset.Exotic.banana)
let privateImage = Image(Asset.private)

// Or as an alternative, you can refer to an enum instance and call .image on it:
let sameBananaImage = Asset.Exotic.banana.image
let samePrivateImage = Asset.private.image

// You can create colors by referring to the enum instance and calling `.color` on it:
let primaryColor = Asset.Theme.primary.color
let backgroundColor = Asset.Theme.background.color

// Or as an alternative, you can use the convenience constructor like this:
let samePrimaryColor = Color(asset: Asset.Theme.primary)
let sameBackgroundColor = Color(asset: Asset.Theme.background)
```

## Further documentation

See [SwiftGen's documentation](https://github.com/SwiftGen/SwiftGen#swiftgen) for full usage and insallation information for the tool itself.

See [SwiftGen's documentation for the `xcassets/swift4.stencil` template](https://github.com/SwiftGen/SwiftGen/blob/master/Documentation/templates/xcassets/swift4.md) for information on the options and generated code available.