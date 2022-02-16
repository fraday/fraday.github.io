# Java BPA Code

My lovely book.

## Files

### Read/Write to Files

Use both the `Scanner` and `File` classes.

```java
//File class
boolean hasNextLine()
boolean createNewFile()

//FileWriter class
FileWriter(String path)
void write(String body)
void close()
```
check for `IOException`s (`java.io.IOException`)
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

<br /><br /><br /><br /><br /><br /><br /><br />




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

Use `<fstream>` with its `ifstream` and `ofstream` classes\n

`file << "text\n";` to write to file (make sure it's open)\n
Be sure to `.close()` your files, and you use `boolean getLine(file, line)` to get/check for a new line `.is_open()` will be a good failsafe.

## String methods
just remember `substr(int pos, int len)` lol

## Important imports

```cpp
#include <iostream> //cout and cin
#include <fstream> //ofstream and ifstream classes
#include <string>
```
