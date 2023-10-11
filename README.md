Welcome to the issue tracker for the [Vault Zero](https://www.vaultzero.app/) iPad/Apple Silicon app.

**File bugs, feature requests and questions [over here](https://github.com/rslifka/vault-zero/issues)**.

## FAQ

### Q: Will there be an Android or iPhone version? You could use Flutter or React Native or...

A: Just to get out ahead of this one: no, sorry; I'm just one person working on this in my spare time 🙂 I realize that narrows down the folks who might find this useful, and that's OK! There's lots of amazing Destiny apps out there on several platforms.

* [Destiny Item Manager](https://destinyitemmanager.com/)
* [BrayTech](https://bray.tech/)
* [D2Foundry](https://d2foundry.gg/)
* [Light.gg](https://www.light.gg/)

### Q: Does this app collect any data or save my information somewhere off my device?

A: Nope, there is no data collection. Your data is stored only on your device and used to make the app go. The only network traffic is between your device and Bungie.

### Q: iPadOS 16.0 and macOS 13.0 are pretty hard pins, can you support earlier versions?

A: It's kinda two questions, and both come down to "I'm just one person". For iPadOS, some SwiftUI components are only available in the latest major version (i.e. 16) and I only have one iPad that auto-updates to the latest iPadOS. That means it's all I can confidently test on. On macOS I have only my MacBook on the latest macOS. "But Slif, there are ways..." I know and I truly appreciate the advice and suggestions, but again - just me. I'd rather invest this time in adding new features and making sure what's there stays up and running.

### Q: What tech did you use?

A: Swift, SwiftUI and CoreData with the phenomenal [AlamoFire](https://github.com/Alamofire/Alamofire) being used for HTTP. Vault Zero is primarily test-driven using [XCTest](https://github.com/apple/swift-corelibs-xctest) with 271 tests as of this writing.

### Q: How long did this take?

A: The first commit was August, 2021 - starting without knowledge of app development nor the languages and technologies required. Here we are, two years and 1,375 commits later...

### Q: How many people contributed?

A: There's one developer (me) but there's no chance I could have shipped this without the great people over at the [unofficial Discord for the Bungie.net API](https://discord.gg/E5uB4BW). Their generosity with their time is truly amazing, and the tools they've built to help Bungie.net API developers are indispensible.

A2: Ted and DJ, thank you! No links, but you know who you are 😃 ❤️

### Q: Could you open-source it?

A: I might!

A2: But if you're Bungie, of course, come on in and have a look around and take everything. It is solely for your game after all, and the assets in the app are all yours 😉
