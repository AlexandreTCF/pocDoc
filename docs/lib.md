# The lib functions

## getFileContentAsString

`getFileContentAsString(path : String): String`

this function allows to get the content of a file 

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

## readCsv

`readCsv(delimiter : String, path : String): Object`

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

## writeJson
## writeFile
## readJson

`readJson(path : String): Object`

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

## writeJsonToCsv

## The array function