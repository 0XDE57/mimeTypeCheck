MIME type check
-

The file `test.gif` has some javascript appended to the end of the file. It is executed when loaded as a script:
```html
<script src="test.gif"></script>
```

1. Download folder locally and open `testload.html` in a browser.
2. If you get a javascript alert, your browser did not enforce MIME type check before executing the .gif

Check console for error message.

Chrome: <br>
`Refused to execute script from '.../test.gif' because its MIME type ('image/gif') is not executable.`

Firefox: <br>
`Loading script from file: URI (“.../test.gif”) was blocked because its MIME type (“image/gif”) is not a valid JavaScript MIME type.`

To fix on Firefox:
1. goto **about:config* 
2. set property `security.block_fileuri_script_with_wrong_mime` to **true**
