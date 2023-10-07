# java-compile-example

### Description

Procedure for creating a compiled jar file using the command line.

The folder "MyApp" contains the MyApp.java file that is to be compiled. The folder "MyAppCompiled" contains the compiled jar file. This was created using the command line on the folder containing the MyApp.java file with the following procedure.

1. Generate a class file "MyApp.class" with the command: 
```
javac MyApp.java
```

2. Create a "Manifest.txt" file using a text editor with the following content. The manifest file is to tell java which class is to be run in the jar file. (note a blank line, carriage-return, is required at the end of the file for it to work with java).  
```
Manifest-Version: 1.0
Main-Class: MyApp

```

3. Generate a "jar" file from the manifest and class files 
```
jar cfm MyApp.jar Manifest.txt MyApp.class
```

4. Execute the jar file using java. The "-cp" argument is shorthand for "class path" and identifies the main class in the jar file as "MyApp". 
```
java -cp MyApp.jar MyApp
```

### Reference:

1. https://stackoverflow.com/questions/9941296/how-do-i-make-a-jar-from-a-java-file
2. https://docs.oracle.com/javase/tutorial/deployment/jar/appman.html
