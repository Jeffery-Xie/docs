## Environment Varibales and File Search ##

### Environment Varibales ###
* declare a variable and use a variable
```
declare tmp_variable
echo ${tmp_variable}
```
**Note** it is better to brace the variable, so the shell does not misunderstand the syntax

* **environment variable** is variable that can pass to child shell process from parent shell process
* **shell variable** is variable that can only be accessed in current shell range
* **export variable** is to export user-defined shell variable into environment variable

## Orders to load environment variable in Linux Shell ##
* ``` /etc/profile，/etc/bashrc``` set system range global environment variable

* ```~/.profile，~/.bashrc``` set private environment variable under user directory

When login system and get a shell process, three steps will execute as orders below:
1. 首先读入的是全局环境变量设定档```/etc/profile```，然后根据其内容读取额外的设定的文档，如 ```/etc/profile.d```, ```/etc/inputrc```

2. 然后根据不同使用者帐号，去其家目录读取```~/.bash_profile```，如果这读取不了就读取```~/.bash_login```，这个也读取不了才会读取 ```~/.profile```，这三个文档设定基本上是一样的，读取有优先关系

3. 然后在根据用户帐号读取```~/.bashrc```

**PS**

~/.profile可以设定本用户专有的路径，环境变量，等，它只能登入的时候执行一次

~/.bashrc也是某用户专有设定文档，可以设定路径，命令别名，每次shell script的执行都会使用它一次

## PATH ##
```PATH``` stores path for shell to look execute program when runs a shell command.

* To have a look at ```PATH```: ``` echo $PATH ```
* To add self-defined path into ```PATH```: ``` export $PATH=$PATH:xxxxxx ```, remember xxxxxx should use absolute path.

**NOTE** while export can only use in shell range and will lose efficacy after current shell is close. To make export last forever:
* add export line to ```.bashrc```

  ``` echo "export $PATH=$PATH:xxxx" >> .bashrc ```

  to make changes applied right now:

  ``` source .bashrc ```

## File Search ##
* ```whereis``` : it can only search binary files using database
* ```locate``` : search files using database
  ``` locate /etc/\*.list ```
* ``` find``` :

  ```find /etc -name '*.list'```
