# JavaBashAPI
java api for linux bash

### Test Case
[mainRun](https://github.com/hello-chenchen/JavaBashAPI/blob/master/qunar/src/com/qunar/mainRun.java)

```java
LinuxCmdFile linuxCmdFile = new LinuxCmdFile("D:/demo/7/README.md");
LinuxCmdFile linuxCmdFile1 = new LinuxCmdFile("D:/demo/7/README1.md");
LinuxCmdDir linuxCmdDir = new LinuxCmdDir("D:/demo/7",LinuxCmdDir.FilterType.SuffixType, ".md");

Set<CommandOption> commandOptionSet = new TreeSet<CommandOption>();
commandOptionSet.add(Cat.CatExecuteOption.optionAndnHandle);
commandOptionSet.add(Cat.CatExecuteOption.optionAndAHandle);

Cat cat = new Cat(commandOptionSet, linuxCmdFile);
Cat cat1 = new Cat(commandOptionSet, "");

Set<CommandOption> commandOptionSet1 = new TreeSet<CommandOption>();
commandOptionSet1.add(Grep.GrepExecuteOption.optionAndnHandle);
commandOptionSet1.add(Grep.GrepExecuteOption.optionAndRHandle);
GrepPattern grepPattern = new GrepPattern("c");
Grep grep = new Grep(grepPattern, commandOptionSet1, "");

Wc wc = new Wc(linuxCmdDir);
Sort sort = new Sort(linuxCmdFile);

CommandHandle commandHandle = new CommandHandle(cat, cat1, sort);
System.out.println(commandHandle.execute());
```
