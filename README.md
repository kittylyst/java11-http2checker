## HTTP2Checker

A simple modular Java 11 tool for checking if sites are running HTTP/2

### Compile

```
$ javac -d out/http2checker src/http2checker/javanut7/ch12/HTTP2Checker.java src/http2checker/module-info.java
```

### Package

```
$ jar -cfe httpchecker.jar javanut7.ch12.HTTP2Checker -C out/http2checker/ .
```

### Run

```
$ java -jar httpchecker.jar http://www.google.com
```

### Link (for custom runtime image)

```
$ jlink --module-path httpchecker.jar:$JAVA_HOME/jmods \ 
--add-modules http2checker \ 
--launcher http2chk=http2checker \ 
--output http2chk-image
```