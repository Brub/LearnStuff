# Finding elements

Er zijn verschillende manieren om elements te vinden.
Je kan hiervoor verschillende locators gebruiken voor iOS.

extra info:
- https://appiumpro.com/editions/8-how-to-find-elements-in-ios-not-by-xpath
- https://appiumpro.com/editions/20-making-your-appium-tests-fast-and-reliable-part-2-finding-elements
- https://appiumpro.com/editions/60-how-to-pick-the-right-locator-strategy

https://github.com/appium/appium-xcuitest-driver#element-location

## Overzicht locators
- Accessibility ID
- id
- name
- class name
- ios predicate string
- ios class chain
- XPath

### Accessibility ID
> When possible, I recommend using the "accessibility ID" locator strategy.
Normally an app developer needs to add these specifically to UI elements in the code.

Here's something surprising: in the XCUITest driver, the accessibility id, id, and name locator strategies are all identical. They are implemented the same way. Go ahead and try switching your locator strategies, you will get the same results. This may change in the future, but for now you can find an element using the name or text in it because iOS has many ways in which it sets a default accessibility identifier if one is not provided by the developer.



### id
> this is actually identical to accessibility id

### name

### class name

### ios predicate string
> Predicate Format Strings are a typical Apple dev thing, and they also work in iOS. 
Predicate format strings enable basic comparisons and matching. 
In our case, they allow basic matching of elements according to simple criteria. 
What's really useful about predicate strings is that you can combine simple criteria to form more complex matches. 
In the XCUITest driver, predicate strings can be used to match various element attributes, including name, value, label, type, visible, etc...

Examples:
`"type == 'XCUIElementTypeCell'"`
`"type == 'XCUIElementTypeButton' AND name == 'Open'"`

https://github.com/facebookarchive/WebDriverAgent/wiki/Predicate-Queries-Construction-Rules

Because predicate matching is built into XCUITest, it has the potential to be much faster than Appium's XPath strategy.

### ios class chain
> The final option is a sort of hybrid between XPath and predicate strings.
This was developed by the Appium team to meet the need of hierarchical queries in a more performant way. 
The types of queries possible via the class chain strategy are not as powerful as those enabled by XPath, but this restriction means a better performance guarantee (this is because it is possible to map class chain queries into a series of direct XCUITest calls, rather than having to recursively build an entire UI tree). 
Class chain queries look very much like XPath queries, however the only allowed filters are basic child/descendant indexing or predicate string matching.

Examples can be found here https://github.com/facebookarchive/WebDriverAgent/wiki/Class-Chain-Queries-Construction-Rules

### XPath
> With the XCUITest driver, it can also be a horrible idea because XPath might be very slow.
XPath and its cousin, XML, are not native languages for iOS development. 
In order to provide access to elements via XPath, the Appium team has had to perform a bunch of technical magic. 
Essentially, every time you run an XPath query, the entire app hierarchy must be recursively walked and serialized into XML. 
This by itself can take a lot of time, especially if your app has many elements. 
Then, once the XPath query has been run on this XML serialization, the list of matching elements must be deserialized into actual element objects before their WebDriver representations are returned to your client call.



