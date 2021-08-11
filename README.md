![](https://github.com/wniemiec-data-java/session/blob/master/docs/img/logo/logo.jpg)

<h1 align='center'>Session</h1>
<p align='center'>Session manager that stores information obtained at run time.</p>
<p align="center">
	<a href="https://github.com/wniemiec-data-java/session/actions/workflows/windows.yml"><img src="https://github.com/wniemiec-data-java/session/actions/workflows/windows.yml/badge.svg" alt=""></a>
	<a href="https://github.com/wniemiec-data-java/session/actions/workflows/macos.yml"><img src="https://github.com/wniemiec-data-java/session/actions/workflows/macos.yml/badge.svg" alt=""></a>
	<a href="https://github.com/wniemiec-data-java/session/actions/workflows/ubuntu.yml"><img src="https://github.com/wniemiec-data-java/session/actions/workflows/ubuntu.yml/badge.svg" alt=""></a>
	<a href="https://codecov.io/gh/wniemiec-data-java/session"><img src="https://codecov.io/gh/wniemiec-data-java/session/branch/master/graph/badge.svg?token=R2SFS4SP86" alt="Coverage status"></a>
	<a href="http://java.oracle.com"><img src="https://img.shields.io/badge/java-11+-D0008F.svg" alt="Java compatibility"></a>
	<a href="https://mvnrepository.com/artifact/io.github.wniemiec-data-java/session"><img src="https://img.shields.io/maven-central/v/io.github.wniemiec-data-java/session" alt="Maven Central release"></a>
	<a href="https://github.com/wniemiec-data-java/session/blob/master/LICENSE"><img src="https://img.shields.io/github/license/wniemiec-data-java/session" alt="License"></a>
</p>
<hr />

## ❇ Introduction
Session manager that stores information obtained at run time. It allows different processes and threads to have access to this information. There are two types of session:

<ul>
	<li>Normal - disk storage</li>
	<li>Shared - storage in class data memory</li> 
</ul>

## ❓ How to use
1. Add one of the options below to the pom.xml file: 

#### Using Maven Central (recomended):
```
<dependency>
  <groupId>io.github.wniemiec-data-java</groupId>
  <artifactId>session</artifactId>
  <version>LATEST</version>
</dependency>
```

#### Using GitHub Packages:
```
<dependency>
  <groupId>wniemiec.data.java</groupId>
  <artifactId>session</artifactId>
  <version>LATEST</version>
</dependency>
```

2. Run
```
$ mvn install
```

3. Use it
```
[...]

import wniemiec.data.java.Session;

[...]

Pair<String, String> example = Pair.of("Hello", "World");

System.out.println( example.getFirst() + " " + example.getSecond() );
```

## 📖 Documentation
|        Method        |Type|Description|Default|
|----------------|-------------------------------|-----------------------------|--------|
|save{,shared} |`key: String, value: Object: void`|Stores data in the current session.| - |
|read{,shared} |`key: String: Object`|Gets data from the current session.| - |
|remove{,shared} |`key: String: void`|Removes data from the current session.| - |
|hasKey{,shared} |`key: String: boolean`|Checks if there is data stored in the session with the specified key.| - |
|destroy{,shared} |`void: boolean`|Deletes the session.| - |

## 🚩 Changelog
Details about each version are documented in the [releases section](https://github.com/williamniemiec/wniemiec-data-java/session/releases).

## 🤝 Contribute!
See the documentation on how you can contribute to the project [here](https://github.com/wniemiec-data-java/session/blob/master/CONTRIBUTING.md).

## 📁 Files

### /
|        Name        |Type|Description|
|----------------|-------------------------------|-----------------------------|
|dist |`Directory`|Released versions|
|docs |`Directory`|Documentation files|
|src     |`Directory`| Source files|
