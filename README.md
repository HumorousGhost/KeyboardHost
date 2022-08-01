# KeyboardHost

This project is only for SwiftUI

When View uses `ignoresSafeArea` or `edgesIgnoringSafeArea(.bottom)`

this framework can be used because `TextField` and `TextEditor` cannot make the keyboard bounce

Encapsulated `UITextView`, `UITextField` can also be used


## Supported Platforms

* iOS 13.0
* macOS 10.15
* tvOS 13.0
* watchOS 6.0

## Usage

```swift
    @State private var text: String = ""
    
    var body: some View {
        VStack {
            Spacer()
            KeyboardHost {
                TextField("please enter text", text: $text)
                    .frame(width: 200, height: 40, alignment: .center)
                    .padding(.bottom, 20)
            }
        }
        .ignoresSafeArea()
    }
```

## Installation

You can add KeyboardHost to an Xcode project by adding it as a package dependency.

1. From the **File** menu, select **Swift Packages** › **Add Package Dependency…**
2. Enter https://github.com/HumorousGhost/KeyboardHost into the package repository URL text field
3. Link **KeyboardHost** to your application target
