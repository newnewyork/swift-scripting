# Swift Scripting
Or How To Write Scripts In Swift

# The Basics 

On the terminal, create a new file for the script and make it executable

	$ touch script.swift
	$ chmod +x script.swift

To make use of the Swift interpreter on runtime, the first line of the script file must be

	#!/usr/bin/swift
	
Now the script can be executed using

	$ ./script.swift
	
The script will run until the last line. To make it stop at a random point, use `exit(0)`.

### Arguments
The arguments used when the script is called can be read by making use of the `CommandLine.arguments` variable. For example, when using
	
	$ ./script.swift -o outputfile

the `CommandLine.arguments` will be

	CommandLine.arguments[0]: ./script.swift
	CommandLine.arguments[1]: -o
	CommandLine.arguments[2]: outputfile

Use`dump(CommandLine.arguments)` to output its contents to the terminal.

### Path
To get the path from where the script is called, import the `Foundation` framework of macOS and make use of its `FileManager` object.

	import Foundation
	let pwd = FileManager.default.currentDirectoryPath







