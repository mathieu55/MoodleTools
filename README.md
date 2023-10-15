# Moodle tools
## SnippetDevTools
Add a customizable tool bar and features in essay question to help students write code. 

Features:
- Enabling tab and shift-tab to indent code 
- Add a button to indent all the codes
- Add buttons to copy to clipboard special character

### How to use it
Create or modify an essay question.
In answer options change answer format to "plain text monospace font"

In question text, click the button HTML with the label "</>".
At the end of the HTML copy all the code from snippetDevTools.html

### How to customize it
To customize the tools, locate the line: "addTools(codeInput,divToolbar,true,true,"{}()<>\"\'&|");"

The third parameter enable/disable indenting with tab and shift-tab 
The fourth parameter add/remove the button to align all the codes
The fifth parameter is the list of special character offers to students to copy to the clipboard.
if the list is empty, the feature is disabled
