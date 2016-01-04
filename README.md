# Log File Highlighter

![alt text][sample]

A Visual Studio Code extension for adding color highlighting to log files. It is based on standard conventions for log4net log files but hopefully it's general enough to be useful for other variations of log files as well. 

The extension associates with `.log` files and applies coloring to the following elements in the file:

* Dates and times in ISO format, such as
	* `2015-12-09`
	* `2015-12-09 09:29`
	* `2015-12-09 09:29:02,258`
* Log level, such as
	* `DEBUG`
	* `INFO`, `INFORMATION`
	* `WARN`, `WARNING`
	* `ERROR`, `FAIL`, `FAILURE`
* Numeric constants, such as
	* `1`
	* `234`
* Standard .Net constants
	* `null`
	* `true`
	* `false`
* String constants, enclosed in single or double quotes. Examples:
	* `"lorem ipsum"`
	* `'lorem ipsum'`
* .Net exception type names, i.e. word ending with `Exception`, such as
	* `ArgumentNullException`
	* `HttpException`
* .Net exception stack traces, i.e. lines starting with whitespace characters, followed by `at`, for example:
	```
	System.NullReferenceException: Object reference not set to an instance of an object.
		at MyClass.DoSomethingElse(string foo)
		at MyClass.DoSomething()
	```



## Change log

### 0.5.11-custom.1, 04 Jan 2016

* Version changed to SemVer compatible
* Merged with master changes from emilast

### 0.5.11, 29 Dec 2015

* A recent VS Code update caused exception call stacks to be uncolored for some reason. Changed so that they use the same color as the exception name.

### 0.5.10, 16 Dec 2015

* Fixed bug that dates were colored the same way as constants.

### 0.5.9.1, 17 Dec 2015

* Added coloring to hex values
* Added my specific log.1, log.2, log.3, log.4, log.5 extensions for rolling logs 
* Date time coloring customized to my specific log requirements

### 0.5.9, 15 Dec 2015

* Added coloring of **string constants** enclosed with single or double quotes.
* Added new constants `null`, `true` and `false`, colored the same way as numeric constants.


[sample]: https://raw.githubusercontent.com/emilast/vscode-logfile-highlighter/master/content/sample.png