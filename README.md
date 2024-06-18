## 在Python中文件操作是非常重要的概念，包括读取、写入、追加、检查文件是否存在，删除以及处理二进制文件
### *1、读取文件*
要读取文件的全部内容，可以使用下面的代码：

`Python`
```python
with open('example.txt', 'r') as file:
    content = file.read()
    print(content)
```
### *2、写入文件*
要将文本写入文件，可以使用下面的代码：
`Python`
```python
with open('example.txt', 'w') as file:
    file.write('Hello, Python!')
```
### *3、追加到文件*
将文本内容现在到现有文件的末尾，可以用下面的代码：
`Python`
```python
with open('example.txt', 'a') as file:
    file.write('\nAppend this line.')
```
### *4、将文件的每一行读取到列表中*
要将文件的每一行读取到列表中，可以使用以下代码：
`python`
```python
with open('example.txt', 'r') as file:
    lines = file.readlines()
    print(lines)
```
[这段代码使用with语句打开文件，并使用readlines()方法将文件的每一行读取到列表中。][1]
### *5、遍历文件的每一行*
要处理文件的每一行，可以使用以下代码：
`python`
```python
with open('example.txt', 'r') as file:
    for line in file:
        print(line.strip())
```
[这段代码使用with语句打开文件，并使用for循环遍历文件的每一行。strip()方法用于删除行尾的换行符][2]
### *6、检查文件是否存在*
要在执行文件操作之前检查文件是否存在，可以使用以下代码：
`python`
```python
import os
if os.path.exists('example.txt'):
    print('File exists.')
else:
    print('File does not exist.')
```

### *7、将列表写入文件*
要将列表的每个元素写入新行，可以使用以下代码：
`python`
```python
lines = ['First line', 'Second line', 'Third line']
with open('example.txt', 'w') as file:
    for line in lines:
        file.write(f'{line}\n')
```
### *8、使用多个文件的with块*
要在执行文件操作之前检查文件是否存在，可以使用以下代码：
`python`
```python
with open('source.txt', 'r') as source, open('destination.txt', 'w') as destination:
    content = source.read()
    destination.write(content)
```
### *9、安全删除文件*
要安全地删除文件（如果存在），可以使用以下代码：
`python`
```python
import os
if os.path.exists('example.txt'):
    os.remove('example.txt')
    print('File deleted.')
else:
    print('File does not exist.')
```
### *10、读取和写入二进制文件*
要读取和写入二进制文件（如图像、视频等），可以使用以下代码：
`python`
```python
# 读取二进制文件
with open('image.jpg', 'rb') as file:
    content = file.read()

# 写入二进制文件
with open('copy.jpg', 'wb') as file:
    file.write(content)
```
[这段代码使用with语句打开二进制文件，并使用read()和write()方法读取和写入文件内容。'b'表示以二进制模式打开文件。][3]
