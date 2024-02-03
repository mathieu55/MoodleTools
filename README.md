# Moodle tools
## SnippetDevTools
Add a customizable tool bar and features in essay question to help students write code. 

![Preview](https://github.com/mathieu55/MoodleTools/blob/main/doc/img/DevToolsPreview.png?raw=true)

Features:
- Enabling tab and shift-tab to indent code 
- Add a button to indent all the codes
- Help using special character (configurable)
  - Button to insert in the answer (recommended, default)
  - Button to send to clipboard (not supported by SEB)
  - List special character for the student to ctrl+c and ctrl+v

### How to use it
Create or modify an essay question.
In answer options change answer format to "plain text monospace font"

In question text, click the button HTML with the label "</>".
At the end of the HTML copy all the code from snippetDevTools.html

### How to customize it
To customize the tools, locate config in the function addTools;

```
let config = {
    enableTab:true, //enable/disable indenting with tab and shift-tab.
    addIndentAll:true, //add/remove the button to align all the codes.
    sepecialChar:{
      lstChar:"{}()[]<>\"\'&|$", //list of special character offers to students
      useClipboard:false, //Only use when useButton:false
                          //true: put special charatere in clipboard (dont work in SEB)
                          //false: insert special charactere in the answer zone

      useButton:true //true: each special char have a button to use it base on the useClipboard
                     //false: each special char is listed as a string. Student can select and ctrl-c + ctrl-v
    }
  }
```