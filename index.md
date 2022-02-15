## Java BPA Code

You can use the [editor on GitHub](https://github.com/fraday/fraday.github.io/edit/main/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Input/Output

Use the `Scanner` class with `System.in`.

```java
import java.util.Scanner;
public class InputOutput {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        int i = sc.nextInt();
        
    }
}
```

### Read/Write to Files

Use both the `Scanner` and `File` classes.

```java
import java.util.File;
import java.util.Scanner;
public class InputOutput {
    public static void main(String[] args) {
        File inputFile = new Filer("path.txt");
        Scanner input = new Scanner(inputFile);
        String fileContents = ""; //Write everything to this file (but no \n's)
        while (input.hasNextLine()) {
            fileContents+=input.nextLine();
        }
        
        
    }
}
```

```java
import java.io.File;  // Import the File class
import java.io.FileWriter;  // Import the FileWriter class
import java.io.IOException;  // Import the IOException class to handle errors

public class CreateFile {
  public static void main(String[] args) {
    try {
      File myObj = new File("filename.txt");
      if (myObj.createNewFile()) {
        System.out.println("File created: " + myObj.getName());
      } else {
        System.out.println("File already exists.");
      }
      FileWriter myWriter = new FileWriter("filename.txt");
      myWriter.write("Files in Java might be tricky, but it is fun enough!");
      myWriter.close();
      System.out.println("Successfully wrote to the file.");
    } catch (IOException e) {
      System.out.println("An error occurred.");
      e.printStackTrace();
    }
  }
}
```
### Method
```java
String substring(int beginIndex, int endIndex)
```
Gets string from beginIndex to but **not including** endIndex
Length of substring will be endIndex-beginIndex
```java
"ABCDEFG".substring(2, 4) //"CD"
```


### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/fraday/fraday.github.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
