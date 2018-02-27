<p align="center">
    <img src="https://github.com/pigfly/A_J_Full_Screen_Image_Browser/blob/master/assets/logo.png?raw=true">
</p>

# A-J-Full-Screen-Image-Browser

![Travis](https://img.shields.io/travis/USER/REPO.svg)
![bitHound](https://img.shields.io/bithound/code/github/rexxars/sse-channel.svg)
![npm](https://img.shields.io/npm/l/express.svg)

A-J-Full-Screen-Image-Browser is an drop-in solution for full screen image and video browser

## Features

- [x] No Dependency, 100% iOS Native
- [x] Support both iPad and iPhone family
- [x] Support image resizing on different screen orientation
- [x] Image can be panned, zoomed and rotated
- [x] Double tap to zoom all the way in and again to zoom all the way out
- [x] Swipe to dismiss
- [x] High level diagram
- [x] MVVM architecture
- [x] Easy to customise

## Requirements

- iOS 8.0+ / macOS 10.10+ / tvOS 9.0+ / watchOS 2.0+
- Xcode 8.3+
- Swift 3.1+

## Installation

- drag and drop the entire `A_J_Full_Screen_Image_Browser` into your project

## Full Usage Example

```swift
import UIKit

final class ViewController: UIViewController {

    lazy var images: [ImageAsyncDownloadable] = {
        return [SingleImage(imageURL: URL(string: "https://images.unsplash.com/photo-1445264918150-66a2371142a2?ixlib=rb-0.3.5&ixid=eyJhcHBfaWQiOjEyMDd9&s=79730c9ec106e3ccee026c648c624e5f&auto=format&fit=crop&w=3800&q=80")!),
                SingleImage(imageURL: URL(string: "https://images.unsplash.com/photo-1483086431886-3590a88317fe?ixlib=rb-0.3.5&s=96129ab02a4a277f5c27273d14323a9a&auto=format&fit=crop&w=3668&q=80")!)]
    }()

    lazy var urls = [URL(string: "https://images.unsplash.com/photo-1502899576159-f224dc2349fa?ixlib=rb-0.3.5&s=4f3943a5d663f9bb062d7d380c8d6fdf&auto=format&fit=crop&w=3700&q=80")!,
                     URL(string: "https://images.unsplash.com/photo-1445264918150-66a2371142a2?ixlib=rb-0.3.5&ixid=eyJhcHBfaWQiOjEyMDd9&s=79730c9ec106e3ccee026c648c624e5f&auto=format&fit=crop&w=3800&q=80")!]

    @IBAction func onButtonTapped(_ sender: UIButton) {
        let vm = FullScreenImageBrowserViewModel(urls: urls)
        let x = FullScreenImageBrowser(viewModel: vm)
        present(x, animated: true, completion: nil)
    }
```


## Demo

<p align="center">
    <img src="https://github.com/pigfly/A_J_Full_Screen_Image_Browser/blob/master/assets/demo.gif?raw=true">
</p>

<p align="center">
    <img src="https://github.com/pigfly/A_J_Full_Screen_Image_Browser/blob/master/assets/demo2.gif?raw=true">
</p>

<p align="center">
    <img src="https://github.com/pigfly/A_J_Full_Screen_Image_Browser/blob/master/assets/demo3.gif?raw=true">
</p>

## HLD

<p align="center">
    <img src="https://github.com/pigfly/A_J_Full_Screen_Image_Browser/blob/master/assets/hld.png?raw=true">
</p>


## Credits

A-J-Full-Screen-Image-Browser is owned and maintained by the [Alex Jiang](https://pigfly.github.io). Thanks [iTMan.design](https://itman.design) for providing computational resources.

## License

A-J-Full-Screen-Image-Browser is released under the MIT license.