# The lib functions

## File function

### getFileContentAsString

`getFileContentAsString(path : String): String`

This function allows to get the content of a file 

**Arguments**

*path*: The relative or absolute path to the file

**Returns**

The content as a string

**Exemple**

```txt
//file.txt
Hello i'm a file
```

```js
getFileContentAsString('file.txt') //=> 'Hello i'm a file'
```

### readCsv

`readCsv(delimiter : String, path : String): Object`

This function allows to get the content parsed of a CSV file  

**Arguments**

*delimiter*: The character that separates the data from a line 
<br>
*path*: The relative or absolute path to the file

**Returns**

The content as a object

**Exemple**

```csv
//file.csv
elm1;elm2
2;'good'
3; 'bad'

```

```js
readCsv(';', 'file.csv')
//=> [ { elm1: '2', elm2: "'good'" }, { elm1: '3', elm2: " 'bad'" } ]
```

### readJson

`readJson(path : String): Object`

This function allows to parse the content of a file JSON

**Arguments**

*path*: The relative or absolute path to the file

**Returns**

The content as a object

**Exemple**

```json5
//file.json
[
  {
    "elm1": "2",
    "elm2": "'good'"
  },
  {
    "elm1": "3",
    "elm2": " 'bad'"
  }
]

```

```js
getFileContentAsString('file.csv')
//=> [ { elm1: '2', elm2: "'good'" }, { elm1: '3', elm2: " 'bad'" } ]
```

### writeFile

`writeFile(path : String, data : Object): void`

This function allows write a data in a file

**Arguments**

*path*: The relative or absolute path to the file who want to create
<br>
*data*: The JS object we want to save

**Exemple**


```js
writeFile('file.txt', 'Some text data\n Some other text data')
//=> file.txt
```

### writeCsv

`writeCsv(path : String, data : Object): void`

This function allows write a data in a CSV file

**Arguments**

*path*: The relative or absolute path to the file who want to create
<br>
*data*: The JS object we want to save

**Exemple**


```js
writeCsv('file.json', [ { elm1: '2', elm2: "'good'" }, { elm1: '3', elm2: " 'bad'" } ])
//=> file.csv
```

### writeJson

`writeJson(path : String, data : Object): void`

This function allows write a data in a JSON file

**Arguments**

*path*: The relative or absolute path to the file who want to create
<br>
*data*: The JS object we want to save

**Exemple**


```js
writeJson('file.json', [ { elm1: '2', elm2: "'good'" }, { elm1: '3', elm2: " 'bad'" } ])
//=> file.json
```

## The array function

### shuffle

`shuffle(array : Array): Array`

This function allows to shuffle an array

**Arguments**

*array*: The array who want to shuffle

**Exemple**


```js
const array = ['a', 'b', 'c', 'd', 'e'];
shuffle(array); //=> [ 'a', 'b', 'd', 'c', 'e' ]
```

### getFirstNthElements

`shuffle(n: Number, array : Array): Array`

This function allows to get N first elements of an array

**Arguments**

*n*: The number of element we want to keep
*array*: The array

**Exemple**


```js
const array = ['a', 'b', 'c', 'd', 'e'];
getFirstNthElements(1, array); //=> [ 'a' ]
getFirstNthElements(3, array); //=> [ 'a', 'b', 'c' ]
```