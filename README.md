# CIPHER

## Introduction

文件加密构件

- 可以对文件进行加密解密
- 使用DES算法加密

## Installation
`maven`

```xml
<dependency>
    <groupId>sse.tongji.bookish-meme</groupId>
    <artifactId>cipher</artifactId>
    <version>1.0.0</version>
</dependency>
```

## Usage
有两种使用方法
- 第一种：
    - 初始化,确定密钥
    ```java
    FileEncryptAndDecrypt fileEncryptAndDecrypt = new FileEncryptAndDecrypt("keyString");
    ```
    - 加密
    ```java
    fileEncryptAndDecrypt.encrypt("./messageRecords/100.log","./messageRecords/100_加密.log");
    ```
    - 解密
    ```java
    fileEncryptAndDecrypt.decrypt("./messageRecords/100_加密.log","./messageRecords/100_解密.log");
    ```
- 第二种：
    - 初始化
    ```java
    FileEncryptAndDecrypt fileEncryptAndDecrypt = new FileEncryptAndDecrypt();
    ```
    - 生成密匙
    ```java
    Key key = fileEncryptAndDecrypt.generateKey("abc");
    ```
    - 用密匙变量加密
    ```java
    fileEncryptAndDecrypt.encrypt("./messageRecords/100.log","./messageRecords/100_加密.log",key);
    ```
    - 用密匙变量解密
    ```java
    fileEncryptAndDecrypt.decrypt("./messageRecords/100_加密.log","./messageRecords/100_解密.log",key);
    ```
