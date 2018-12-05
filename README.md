# JalapenoTiles

[![Version](https://img.shields.io/cocoapods/v/JalapenoTiles.svg?style=flat)](https://cocoapods.org/pods/JalapenoTiles)
[![License](https://img.shields.io/cocoapods/l/JalapenoTiles.svg?style=flat)](https://cocoapods.org/pods/JalapenoTiles)
[![Platform](https://img.shields.io/cocoapods/p/JalapenoTiles.svg?style=flat)](https://cocoapods.org/pods/JalapenoTiles)

## Example

To run the example project, clone the repo, and run `pod install` from the Example directory first.

## Requirements

iOS 10.0+
Xcode 10.0+

## Installation

JalapenoTiles is available through [CocoaPods](https://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod 'JalapenoTiles'
```

## Usage

1. Import JalapenoTiles in the view where you want to use it:

```
import JalapenoTiles
```

2. Create Array with JalapenoModel in which you declare all items displayed in Tails.

```
let data = [JalapenoModel(id: "1",title: "First Item", imageName: "ImageName", price: 10.99), 
            JalapenoModel(id: "2",title: "Second Item", imageName: "ImageName", price: 29.99)]
```

`id` : String - identifier (to find later Your item in a basket)
`title` : String - title displayed in cell
`imageName`: String - image name wich displayed in cell
`price`: Double - number displayed on right top in cell

3. Create an instance of `JalapenoTilesView` with the data created above:

```
let jalapenioCollectionView = JalapenoTilesView(data: data)
```

4. Use autolayout or another code based method to set up sizes (I use VFL):

```
self.view.addConstraintsWithFormat(format: "H:|[v0]|", views: jalapenioCollectionView)
self.view.addConstraintsWithFormat(format: "V:|[v0]|", views: jalapenioCollectionView)
```

## Customization

`showPriceTags`: Bool - Responsible for that if you want the price tag to be displayed or not.
`textColor`: UIColor - Changes the title label color in the cell.
`accentColor`: UIColor - Chanes the price label, count label and buttons (add,remove) color in the cell

## Author

Namedix, bartek.pichalski@appnroll.com

## License

JalapenoTiles is available under the MIT license. See the LICENSE file for more info.
