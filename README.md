 
#Toothpick *(a.k.a T.P. like a teepee)*


<table style="border:0px">
  <tr  style="border:0px">
    <td width="125" style="border:0px">
      <img src="https://raw.github.com/stephanenicolas/toothpick/master/assets/logo.jpg" width="125px" /> 
    </td>
    <td  style="border:0px">
      <a alt="Build Status" href="https://travis-ci.org/stephanenicolas/toothpick">
      <img src="https://travis-ci.org/stephanenicolas/toothpick.svg?branch=master"/></a>
      <br/>
      <a alt="Coverage Status" href="https://coveralls.io/github/stephanenicolas/toothpick?branch=master">
      <img src="https://coveralls.io/repos/github/stephanenicolas/toothpick/badge.svg?branch=master"/></a>
    </td>
  </tr>
</table>

## What is ToothPick ?
 
 
ToothPick is a tree scope based Dependency Injection (DI) library.

It is a full-featured, runtime based implementation of [JSR 330](https://jcp.org/en/jsr/detail?id=330).

## What does ToothPick offer ?

```
//a typical Toothpick scope tree during the execution of an Android app.

       @ApplicationSingleton 
         /              |    \  
        /               |     \
       /                |      \
   @PresenterSingleton  |   Service 2
         /              | 
        /            Service 1  
       /            
Activity 1
    /   \
   /   Fragment 2
  /
Fragment 1
```

ToothPick is :
* pure java
* fast, it doesn't use reflection but annotation processing
* flexible, extensible & powerful, robust & tested
* test oriented
* thread safe
* documented & Open Source 
* it works very well with Android or any other context based framework (such as web containers)

Hey, Android Devs, you can use TP to [create MVP apps so easily](https://github.com/stephanenicolas/toothpick/blob/master/smoothie-sample/src/main/java/com/example/smoothie/RxMVPActivity.java) !


## Examples

Currently Toothpick has 2 sets of examples : 
* one [in pure Java](https://github.com/stephanenicolas/toothpick/tree/master/toothpick-sample)
* one [for Android](https://github.com/stephanenicolas/toothpick/tree/master/smoothie-sample)

## Setup
For Android : 
```
#android setup using apt 
buildscript {
  repositories {
    mavenCentral()
  }
  dependencies {
    classpath 'com.neenbedankt.gradle.plugins:android-apt:1.8'
  }
}
dependencies {
  compile 'toothpick:toothpick-runtime:x.y.z') //or 'toothpick:smoothie:x.y.z'
  apt 'toothpick:toothpick-compiler:x.y.z')
  testCompile 'toothpick:toothpick-testing:x.y.z') //highly recommended
  testCompile 'mockito or easymock'
}
```

For java:
```
<!--java setup with maven -->
  <dependencies>
    <dependency>
      <groupId>toothpick</groupId>
      <artifactId>toothpick-compiler</artifactId>
      <version>x.y.z</version>
      <scope>compile</scope>
    </dependency>
    <dependency>
      <groupId>toothpick</groupId>
      <artifactId>toothpick-runtime</artifactId>
      <version>x.y.z</version>
      <scope>compile</scope>
    </dependency>
    <dependency> <!-- highly recommended-->
      <groupId>toothpick</groupId>
      <artifactId>toothpick-testing</artifactId>
      <version>x.y.z</version>
      <scope>test</scope>
    </dependency>
    <dependency>
    <easymock or mockito>
    </dependency>
  </dependencies>
```

# Wanna know more ?

Visit [ToothPick's wiki](https://github.com/stephanenicolas/toothpick/wiki) !




