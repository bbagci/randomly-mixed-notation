# Randomly mixed notation

Encodes randomly every character either into their decimal or hexadecimal numeric character reference, see <https://bbagci.net/randomly-mixed-notation>

You can use following snippet:

```javascript
function randomlyMixedNotation(rawStr) {
    let sb = ""
    for (let index = 0; index < rawStr.length; index++) {
        if (Math.random() < 0.5) {
            sb += "&#" + rawStr.charCodeAt(index) + ";"
        } else {
            sb += "&#x" + rawStr.charCodeAt(index).toString(16) + ";"
        }
    }
    return sb
}
```