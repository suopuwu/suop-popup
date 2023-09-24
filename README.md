
# suop-popup
A highly customizable vanilla js popup solution with beautiful animations and built in functionality.

## Installation
Simply include the js file in a script tag like so:
``<script  src="suopPopup.js"  defer></script>``
## Usage
To create a popup, simply make a new instance of SuopPopup like so:
``let popup = new SuopPopup("Content", {deleteOnClose: false})``
Make sure to toggle it so the popup displays.
``popup.toggle()``
### Options
The SuopPopup class has two parameters: content and options. Content is an HTML string, and options is an  object with the properties listed below:
|Name | Data type | Default value | Notes |
|--|--|--|--|
| deleteOnClose | Boolean | true | Only affects when the popup is closed by the user clicking out of its bounds. |
| background | String | null | The popup's background color ie. 'white' or '#abc123' |
| confirm | Function or null | null | If not null, adds a confirm button to the bottom of the popup. calls the function when the button is clicked. |
| cancel | Function or null | null| See above |
| borderRadius | Number | 10 | |
| padding | Number | 10 | |
| floating | Boolean | false | If false, centers the popup and darkens the background. If true, spawns a floating popup similar to a right click menu. |
| x | Number or null | null | When popup is floating, determines the x position of the popup. |
| y | Number or null | null | When popup is floating, determines the y position of the popup. |
| shadow | string | '0 14px 28px rgba(0,0,0,0.25), 0 10px 10px rgba(0,0,0,0.22)' | The css string used to style the popup's shadow. |
You only have to specify the options you use, the rest will be filled in automatically.
### Methods
A suop popup has the following methods
| Name | Description |
|--|--|
| toggle() | Toggles the visibility of the popup. |
| showPopup() | Shows the popup. |
| hidePopup() | Hides the popup. |
| remove(delay) | Deletes the Html node of the popup after a specified number of miliseconds. |
| hideThenDelete() | Hides the popup, then deletes it after the hiding animation has completed (200ms) |
### Getters & Setters
You can get and set the content value of the suopPopup, and it will update the html.
```
let popup = new SuopPopup('Test content')
console.log(popup.content)
popup.content = 'new content'
console.log(popup.content)
```
