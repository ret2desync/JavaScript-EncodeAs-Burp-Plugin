# JavaScript-EncodeAs-Burp-Plugin
Version 1.0.

The JavaScript EncodeAs Burp Plugin allows you to encode strings in the JavaScript format (i.e. Unicode/Hex), similar to Burp's Convert-To but specifically for within JSON/JavaScript.

Can be useful for bypassing WAF's/web application validation, particularly if the value is later returned as is and read by JavaScript in the browser.

Supports three types of encoding:
- Unicode (\uHHHH)
- Unicode Aware (\u{H-HHHHHH})
- Hex (\xHH)
## Installation
1. Download the plugin [javascript-encodeas.py](https://raw.githubusercontent.com/ret2desync/JavaScript-EncodeAs-Burp-Plugin/main/javascript-encodeas.py)
2. Set up Jython in Burp Suite by going to the Extender tab and selecting the Options subtab. Under the "Python Environment" section, select "Use existing Jython standalone JAR" and browse to the location of the Jython standalone JAR on your computer
3. In Burp Suite, go to the Extender tab and click on the "Add" button.
4. Select "Python" as the extension type and select the javascript-encodeas.py file from your computer.

## Usage
In places where you can modify text (For example Repeater, Intruder):

Right Click -> Extensions -> JavaScript EncodeAs -> (Choose Encoding Choice)

Text should be encoded in JavaScript friendly format

Encoding Choices:

* Unicode Encode Non-Alpha (\u0061abcd)

   Unicode Encodes Non-Alpha Characters, for example:

   `<script>alert(1)</script> -> \u003Cscript\u003Ealert\u00281\u0029\u003C\u002Fscript\u003E`

* Unicode Encode All Characters (\\u0061)

   Unicode Encodes All Characters, for example:

   `<script>alert(1)</script> -> \u003C\u0073\u0063\u0072\u0069\u0070\u0074\u003E\u0061\u006C\u0065\u0072\u0074\u0028\u0031\u0029\u003C\u002F\u0073\u0063\u0072\u0069\u0070\u0074\u003E`

* Unicode Aware Encode Non-Alpha (\\u{61}abcd)

   Unicode Aware Encodes Non-Alpha Characters, for example:

   `<script>alert(1)</script> -> \u{3c}script\u{3e}alert\u{28}1\u{29}\u{3c}\u{2f}script\u{3e}`

* Unicode Aware Encode All Characters (\\u{61})

   Unicode Aware Encodes All Characters, for example:

   `<script>alert(1)</script> -> \u{3c}\u{73}\u{63}\u{72}\u{69}\u{70}\u{74}\u{3e}\u{61}\u{6c}\u{65}\u{72}\u{74}\u{28}\u{31}\u{29}\u{3c}\u{2f}\u{73}\u{63}\u{72}\u{69}\u{70}\u{74}\u{3e}`

* Hex Encode Non-Alpha (\\x61abcd)

   Hex Encodes Non-Alpha Characters for example:

   `<script>alert(1)</script> -> \x3Cscript\x3Ealert\x281\x29\x3C\x2Fscript\x3E`

* Hex Encode All Characters (\\x61)

   Hex Encodes All Characters for example:

   `<script>alert(1)</script> -> \x3C\x73\x63\x72\x69\x70\x74\x3E\x61\x6C\x65\x72\x74\x28\x31\x29\x3C\x2F\x73\x63\x72\x69\x70\x74\x3E`
## Demo
[Demo.gif](https://raw.githubusercontent.com/ret2desync/JavaScript-EncodeAs-Burp-Plugin/main/demo/burp-plugin-demo.gif)
## Feedback
If you have any feedback or suggestions, feel free to open an issue on this Github repository.

## License
This plugin is licensed under the MIT License.
