# Java BPA Code

My lovely book.

## Files

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
<br />
## Methods
### Strings
```java
String substring(int beginIndex, int endIndex)
```
Gets string from `beginIndex` to but **not including** `endIndex`
Length of substring will be `endIndex-beginIndex`

<br />

```java
int codePointAt(int index) 
```
Returns unicode of character at specified index. `codePointBefore(int index)` is also a defined function.

<br />

```
%c 	Format characters
%d 	Format decimal (integer) numbers (base 10)
%e 	Format exponential floating-point numbers
%f 	Format floating-point numbers
%i 	Format integers (base 10)
%o 	Format octal numbers (base 8)
%s 	Format string of characters
%u 	Format unsigned decimal (integer) numbers
%x 	Format numbers in hexadecimal (base 16)
%n 	add a new line character
```
printf() symbols

<br />

**Self-explanatory definitions**
```java
boolean isEmpty()
```
```java
int firstIndexOf(String check)
int lastIndexOf(String check)
```
```java
String[] split(String check)
```
```java
boolean matches(String regex) //AUTOPUTS "^ $" AROUND
```
```java
char[] toCharArray()
```
<br /><br /><br />





# C++ Resources

## Vectors
### Constructor definitions
default (1)	
`explicit vector (const allocator_type& alloc = allocator_type());`

fill (2)	
`explicit vector(size_type n, const value_type& val = value_type(), const allocator_type& alloc = allocator_type());`

range (3)	
`template <class InputIterator> vector(InputIterator first, InputIterator last, const allocator_type& alloc = allocator_type());`

copy (4)	
`vector (const vector& x);`

```cpp
std::vector<int> first;                                // empty vector of ints
std::vector<int> second (4,100);                       // four ints with value 100
std::vector<int> third (second.begin(),second.end());  // iterating through second
std::vector<int> fourth (third);                       // a copy of third
```
<br />
### Method definitions

```cpp
T at(int index)
int length()
int find (const string& str, int pos = 0) const;
iterator insert (iterator position, const value_type& val);
int size()
void clear()
```



## Read/Write to files

Use `<fstream>` with its `ifstream` and `ofstream` classes
```cpp
// reading a text file
#include <iostream>
#include <fstream>
#include <string>
using namespace std;

int main () {
  string line;
  ifstream myfile ("example.txt");
  if (myfile.is_open())
  {
    while ( getline (myfile,line) )
    {
      cout << line << '\n';
    }
    myfile.close();
  }

  else cout << "Unable to open file"; 

  return 0;
}
```
```cpp
// writing on a text file
#include <iostream>
#include <fstream>
using namespace std;

int main () {
  ofstream myfile ("example.txt");
  if (myfile.is_open())
  {
    myfile << "This is a line.\n";
    myfile << "This is another line.\n";
    myfile.close();
  }
  else cout << "Unable to open file";
  return 0;
}
```
Be sure to `.close()` your files, and you use `boolean getLine(file, line)` to get/check for a new line `.is_open()` will be a good failsafe.

## String methods
just remember `substr(int pos, int len)` lol

## Important imports

```cpp
#include <iostream> //cout and cin
#include <fstream> //ofstream and ifstream classes
#include <string>
```
