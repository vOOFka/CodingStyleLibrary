# CodingStyleLibrary

This library contains one propertywrapper to dynamically convert a string to a string with the appropriate formatting type. The library currently supports the following styles: camelCase snake_case kebab-case.

# For example:

Camel case style: "Hello big world!" -> "helloBigWorld!"
Snake case style: "Hello big world!" -> "hello_big_world!"
Kebab case style: "Hello big world!" -> "hello-big-world!"

![](CodingStyleLibrary_example.gif)

# Usage example:

import SwiftUI
import CodingStyleLibrary

struct SomeSwiftUIView: View {
    @CodingStyle(typeStyle: .kebabCase) var username: String = ""
    
    var body: some View {
        TextField(
            "User name (email address)",
            text: $username)
    }
}
