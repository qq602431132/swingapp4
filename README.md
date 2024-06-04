# swingapp4
graalvm Linux swing native image input Chinese 

Import the program directory into netbeans and  package the executable jar file.
```
JDK Version
mxh@mxh:~/Desktop$ java -version
java version "22.0.1" 2024-04-16
Java(TM) SE Runtime Environment Oracle GraalVM 22.0.1+8.1 (build 22.0.1+8-jvmci-b01)
Java HotSpot(TM) 64-Bit Server VM Oracle GraalVM 22.0.1+8.1 (build 22.0.1+8-jvmci-b01, mixed mode, sharing)
mxh@mxh:~/Desktop$ which java
/home/mxh/Downloads/jdks/graalvm-jdk-22.0.1+8.1/bin/java
mxh@mxh:~/Desktop$ 
```

1.cd /home/mxh/NetBeansProjects/swingapp4/dist  

2.java -agentlib:native-image-agent=config-output-dir=config -jar swingapp4.jar

3.native-image --no-fallback -march=native -H:+AddAllCharsets -H:ConfigurationFileDirectories=config --enable-url-protocols=https,http -Djava.awt.headless=false -Djdk.gtk.version=2 -Dsun.java2d.debugfonts=true --allow-incomplete-classpath --add-exports java.desktop/sun.font=ALL-UNNAMED -J-Xmx16G -jar swingapp4.jar



Then ./swingapp4 execut program, using fcitx sunpin to input Chinese, found unable to input Chinese.


The dependent software is as follows:
