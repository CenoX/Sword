# Sword
A Swift Package for the Discord API - **This is very early in development**

## Install - You can't yet lel
In order to include Sword as a dependency, you need to have macOS (Linux soon), Swift 3.0, and an internet connection
```swift
let package = Package(
    name: "yourswiftexecutablenamehere",
    dependencies: [
        .Package(url: "https://github.com/Azoy/Sword", Version(0, 0, 44))
    ]
)
```

## Example
```swift
import Sword

let bot = Sword(token: "tokenhere")

bot.on("messageCreate") { msg in
  let msg = (msg as! [Message])[0]
  if msg.content == "!ping" {
    bot.send("Pong!", to: msg.channelId)
  }
}

bot.connect()
```