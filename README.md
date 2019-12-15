# Felix language support for the Sublime Text editor

This package provides syntax highlighting for the [Felix programming language](http://felix-lang.org/).

Currently, only simple syntax highlighting is provided. Please contribute if you would like to add more editing support.

## Installation

This package can be installed via [Sublime Package Control](https://sublime.wbond.net/). If Package Control is installed already, you can simply:

* Open the Command Pallete (`ctrl+shift+P` or `cmd+shift+P`).
* Type "Install Package" and hit return.
* Type "Felix" and hit return.

If not, Package Control can be installed following [these simple instructions](https://packagecontrol.io/installation) 

If you wish to install manually, you can clone this repository in your [Sublime Text Packages](http://docs.sublimetext.info/en/latest/basic_concepts.html#the-packages-directory).

Next time you open a script with the `.flx` extension, Sublime Text will properly syntax highlight the code.


## Binding `cmd+/' to comment out current or selected line(s)

Create a `Comments.tmPreferences` XML file in `Packages/User` (`~/Library/Application Support/Sublime Text 3/Packages/User` in MacOS) with the following code. If the file exists already, add the outer `<dict>` block to it.

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple Computer//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
    <key>name</key>
    <string>Comments</string>
    <key>scope</key>
    <string>source.felix</string>
    <key>settings</key>
    <dict>
        <key>shellVariables</key>
        <array>
            <dict>
                <key>name</key>
                <string>TM_COMMENT_START</string>
                <key>value</key>
                <string>// </string>
            </dict>
            <dict>
                <key>name</key>
                <string>TM_COMMENT_START_2</string>
                <key>value</key>
                <string>{/* </string>
            </dict>
            <dict>
                <key>name</key>
                <string>TM_COMMENT_END_2</string>
                <key>value</key>
                <string> */}</string>
            </dict>
        </array>
    </dict>
    <key>uuid</key>
    <string>F9BFFF1F-1999-4722-B094-52E8AFD234D1</string>
</dict>
</plist>
```
