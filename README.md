# spark-challenge

## Links

- [Repo](https://github.com/malli9999/spark-challenge/tree/master/src)


## Prerequisites

- VS Code
- VS Code Extension: Maven for Java
- VS Code Extension: Java Extension Pack

## Instructions 1 - Start New Maven Project

1. Create a new project using Maven (you do not need to fork this repo).
1. There should be a folder on your laptop where you keep your git projects. Go to this folder, e.g. 44517.
1. Open this parent folder in VS Code.
1. Click the VS Code Extensions icon. Verify you have the two required extensions. If not, install them.
1. Click the VS Code Explorer icon. From the menu, select:
1. View / Command Palette / Maven: Create Maven Project / archetype-quickstart-jdk8 / most recent version.
1. When the folder window opens, click your parent folder up at the top, click "Select Destination Folder".

## Instructions 2 - Interactive Mode

```Bash
groupId: edu.nwmissouri.arjun
artifactId: spark-challenge
version: HIT ENTER
package: HIT ENTER
Y: HIT ENTER
```

You will now have a spark-challenge project folder. Exit VS Code.

## Instructions 3 - Code the project

Change directory into your new spark-challenge folder. Right-click and open your spark-challenge folder in VS Code.

Add a basic README.md. Use it to store your notes and commands.

When VS Code asks: "A build file was modified. Do you want to synchronize the Java classpath/configuration?" Answer "Always" to allow VS Code to generate these artifacts automatically.

## Instructions 4 - Add to POM.xml

Copy the POM.xml from this repo to yours. Use CTRL-F to search for "isl" for "Intelligent Systems Lab".
Change each occurance to match yourname in your groupId instead.

## Prepare the Code

```PowerShell
mvn clean
mvn compile
mvn assembly:single
```

## Execute

```Bash
java -cp target/spark-challenge-1.0.0-jar-with-dependencies.jar edu.nwmissouri.arjun.App "data.txt"
```

## Challenges - Getting Started

1. Where does program execution begin?
1. Update the main method to check that exactly one argument is provided.
1. If not, output a message and call System.exit(0);
1. If so, call a new method named process that uses the first item in the arg array.
1. Add the following imports to App.java.

```Java
import org.apache.spark.SparkConf;
import org.apache.spark.api.java.JavaPairRDD;
import org.apache.spark.api.java.JavaRDD;
import org.apache.spark.api.java.JavaSparkContext;
import scala.Tuple2;
import java.util.Arrays;
import java.nio.file.FileSystems;
import java.nio.file.Path;
import java.util.Comparator;
```


    
