# KeyboardHost

This project is only for SwiftUI

When View uses `ignoresSafeArea` or `edgesIgnoringSafeArea(.bottom)`

this framework can be used because `TextField` and `TextEditor` cannot make the keyboard bounce

Encapsulated `UITextView`, `UITextField` can also be used

### Demo

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
