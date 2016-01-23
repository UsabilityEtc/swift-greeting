# swift-greeting

A simple Swift package that's used by the [swift-hello-world](https://github.com/UsabilityEtc/swift-hello-world) example to illustrate adding a Swift package as a dependency.

The package has the following definition in `Package.swift`:

```
import PackageDescription

let package = Package(
    name: "SwiftGreeting"
)
```

and provides the `Greeting` class in `Greeting.swift`:

```
public class Greeting {

  var greeting = "Hello"

  init() {}

  public init(greeting: String) {
    self.greeting = greeting
  }

  public func outputGreeting() {
    print(greeting)
  }

}
```

The `Greeting` class, it's `init(greeting: String)` and the `outputGreeting` method need to be public to enable them to be referenced in the package that imports this package with:

```
import SwiftGreeting
```
