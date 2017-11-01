English | [한국어](README-KR.md)

# markdown_navigator

**markdown_navigator** creates a link to quickly navigate to all the files in your folder.

Use it to quickly create index where markdown is used, such as "github".

![example](example.PNG)

## Installation 
```bash
$ npm install -g markdown_navigator
```
## Usage
```bash
$ mdnv create [foler_name] [options]
```
```bash
$ mdnv --help
usage: mdnv create [foler_name] [options]

folder_name:   The name of the folder where you want to create the index

options:
  -n name      The name of the index file to be created. default is "index"
  -h, --help   You're staring at it
```


### Basic
If only the default command is entered,  
creates a 'index.md' for all files within the currently located folder.
```
$ mdnv create
```


### Example  
**example folder**
```
test_folder
|-- file1.md
|-- folder
|   |-- file2.md
|   |-- file3.md
```
<br/>

**basic example**
```bash
$ cd test_folder/
$ mdnv create
```
`index.md` is created with the following contents.
```
[file1.md](/file1.md)
[file2.md](/folder/file2.md)
[file3.md](/folder/file3.md)
```
<br/>  

**option example**  
This is an example of adding `folder_name` and `-n` options.
```bash
$ cd test_folder/
$ mdnv create folder -n menu
```
`index.md` is created with the following contents.
```
[file2.md](/folder/file2.md)
[file3.md](/folder/file3.md)
```

## Version

**current verstion : 0.1.0**  

[change log](CHANGELOG.md)

## License

Licensed under [MIT License](LICENSE). © minung.han
