# Reading & Writing Files

> ### What is a file?

1. **Header** - *Metadata (file name, size, type, etc)*
2. **Data** - *Contents of the file*
3. **EOF** - *End of file*(special character)

> ### File Paths

1. **Folder Path** - *Main folder location start place*
2. **File Name** - *Actual name of file
3. **Extension** - *After the "." in a file name.*

> ### Line Endings

*ASA standard states that line endings should use the sequence of the Carriage Return (CR or \r) and the Line Feed (LF or \n) characters (CR+LF or \r\n). The ISO standard however allowed for either the CR+LF characters or just the LF character.*

> #### character encodings
*The two most common encodings are the ASCII and UNICODE Formats. ASCII can only store 128 characters, while Unicode can contain up to 1,114,112 characters.*

### Open & Close Files

1. In Python use a **TRY-FINALLY** block
```
eader = open('dog_breeds.txt')
try:
    # Further file processing goes here
finally:
    reader.close()
```
2. Also use a **WITH** statement
```
with open('dog_breeds.txt') as reader:
    # Further file processing goes here
```
3. Using **second** arguement parameter
```
with open('dog_breeds.txt', 'r') as reader:
    # Further file processing goes here
```
|Character|Meaning|   
|---|---|
|r|Open for reading(*Default*)|
|w|Open for writing, truncating (overwriting) the file first| 
|rb, wb|Open in binary mode (read/write using byte data)|

### Files are objects
1. **Text Files** - *Most common type*
```
open('abc.txt')
open('abc.txt', 'r')
open('abc.txt', 'w')
```
2. **Buffered Binary Files** - *used for reading and writing binary files*
```
open('abc.txt', 'rb')
open('abc.txt', 'wb')

>>> file = open('dog_breeds.txt', 'rb')
>>> type(file)
<class '_io.BufferedReader'>
>>> file = open('dog_breeds.txt', 'wb')
>>> type(file)
<class '_io.BufferedWriter'>
```
3. **Raw Binary Files** - *used as a low-level building-block for binary and text streams*
```
open('abc.txt', 'rb', buffering=0)

>>> file = open('dog_breeds.txt', 'rb', buffering=0)
>>> type(file)
<class '_io.FileIO'>
```

### Reading & Writing Opened Files
1. **Reading Files**

|Method|What it does|
|---|---|
|.read(size=-1)|This reads from the file based on the number of size bytes. If no argument is passed or None or -1 is passed, then the entire file is read.|
|.readline(size=-1)|This reads at most size number of characters from the line. This continues to the end of the line and then wraps back around. If no argument is passed or None or -1 is passed, then the entire line (or rest of the line) is read.| 
|.readlines()|This reads the remaining lines from the file object and returns them as a list.|

**.read()**
```
>>> with open('dog_breeds.txt', 'r') as reader:
>>>     # Read & print the entire file
>>>     print(reader.read())
Pug
Jack Russell Terrier
English Springer Spaniel
German Shepherd
Staffordshire Bull Terrier
Cavalier King Charles Spaniel
Golden Retriever
West Highland White Terrier
Boxer
Border Terrier
```
**.readline()**
```
>>> with open('dog_breeds.txt', 'r') as reader:
>>>     # Read & print the first 5 characters of the line 5 times
>>>     print(reader.readline(5))
>>>     # Notice that line is greater than the 5 chars and continues
>>>     # down the line, reading 5 chars each time until the end of the
>>>     # line and then "wraps" around
>>>     print(reader.readline(5))
>>>     print(reader.readline(5))
>>>     print(reader.readline(5))
>>>     print(reader.readline(5))
Pug

Jack
Russe
ll Te
rrier
```
**readlines()**
```
>>> f = open('dog_breeds.txt')
>>> f.readlines()  # Returns a list object
['Pug\n', 'Jack Russell Terrier\n', 'English Springer Spaniel\n', 'German Shepherd\n', 'Staffordshire Bull Terrier\n', 'Cavalier King Charles Spaniel\n', 'Golden Retriever\n', 'West Highland White Terrier\n', 'Boxer\n', 'Border Terrier\n']
```
**list()**
```
>>> f = open('dog_breeds.txt')
>>> list(f)
['Pug\n', 'Jack Russell Terrier\n', 'English Springer Spaniel\n', 'German Shepherd\n', 'Staffordshire Bull Terrier\n', 'Cavalier King Charles Spaniel\n', 'Golden Retriever\n', 'West Highland White Terrier\n', 'Boxer\n', 'Border Terrier\n']
```

### Iterating over lines in a file
```
>>> with open('dog_breeds.txt', 'r') as reader:
>>>     # Read and print the entire file line by line
>>>     for line in reader:
>>>         print(line, end='')
Pug
Jack Russell Terrier
English Springer Spaniel
German Shepherd
Staffordshire Bull Terrier
Cavalier King Charles Spaniel
Golden Retriever
West Highland White Terrier
Boxer
Border Terrier
```

### Writing to a file

|Method|What it does|   
|---|---|
|.write(string)|This writes the string to the file.|
|.writelines(seq)|This writes the sequence to the file. No line endings are appended to each sequence item. It’s up to you to add the appropriate line ending(s).| 
**Example**
```
    # Note: readlines doesn't trim the line endings
    dog_breeds = reader.readlines()

with open('dog_breeds_reversed.txt', 'w') as writer:
    # Alternatively you could use
    # writer.writelines(reversed(dog_breeds))

    # Write the dog breeds to the file in reversed order
    for breed in reversed(dog_breeds):
        writer.write(breed)
```
