# java-compile-example

### Description

Procedure for creating a compiled jar file using the command line.

The folder "MyApp" contains the MyApp.java file that is to be compiled. The folder "MyAppCompiled" contains the compiled jar file.

1. Create a file "MyApp.class" with the command: <br/>
`javac MyApp.java`

2. Create a Manifest.txt file with the following content (note a blank line, carriage-return, is required for it to work). The manifest file is to tell java which class is to be run in the jar file. <br/>
`Manifest-Version: 1.0` <br/>
`Main-Class: MyApp`<br />
` `

3. Create a "jar" file from the manifest and class files <br/>
`jar cfm MyApp.jar Manifest.txt MyApp.class`

4. Execute the jar file using java: <br/>
`java -cp MyApp.jar MyApp`

Reference:

1. https://stackoverflow.com/questions/9941296/how-do-i-make-a-jar-from-a-java-file
2. https://docs.oracle.com/javase/tutorial/deployment/jar/appman.html
