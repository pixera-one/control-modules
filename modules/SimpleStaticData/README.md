# SimpleStaticData

A simple module that acts as a placeholder for a static data field.
The data that is inserted will be passed to the output when the action is triggered.
The data string needs to beginn and end with double quotes " or single quotes '

If special characters , formatting or quotes are required inside the string be advised that the formatting will follow the JSON rules:
https://pixera.helpjuice.com/en_US/ui-elements/data-entry-with-quotation-marks-and-other-special-characters

"Hello" World => "\"Hello\" World"
preset:"page1"&title:"Hello" => "preset:\"page1\"&title:\"Hello\""
Hallo\World => "Hallo\\World"
Hello
World => "Hello\nWorld"

Further Documentation: www.json.org
check the right tab under "escape"
