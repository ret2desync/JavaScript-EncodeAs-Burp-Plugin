# JavaScript-EncodeAs-Burp-Plugin
Version 1.0
The JavaScript EncodeAs Burp Plugin allows you to encode strings in the JavaScript format (i.e. Unicode/Hex), similar to Burp's Convert-To but specifically for within JSON/JavaScript.

Can be useful for bypassing WAF's/web application validation, particularly if the value is later returned as is and read by JavaScript in the browser.

Supports three types of encoding:
- Unicode (\uXXXX)
- Unicode Aware (\u{X-XXXXX})
- Hex (\xXX)
## Installation
1. Download the plugin [javascript-encodeas.py](https://raw.githubusercontent.com/akashc99/JSON-Escaper-Burp-Suite-Python-plugin/main/javascript-encodeas.py)
2. Set up Jython in Burp Suite by going to the Extender tab and selecting the Options subtab. Under the "Python Environment" section, select "Use existing Jython standalone JAR" and browse to the location of the Jython standalone JAR on your computer
3. In Burp Suite, go to the Extender tab and click on the "Add" button.
4. Select "Python" as the extension type and select the javascript-encodeas.py file from your computer.

## Usage



## Feedback
If you have any feedback or suggestions, feel free to open an issue on this Github repository.

## License
This plugin is licensed under the MIT License.
