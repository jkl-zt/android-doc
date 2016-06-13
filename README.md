# android-doc
##### ButterKnife 8.0.1版本
------
######AndroidStudio中ButterKnife时出现问题
add apt
``````
buildscript {
    repositories {
        jcenter()
    }
    dependencies {
        classpath 'com.android.tools.build:gradle:2.1.0'
        classpath 'com.neenbedankt.gradle.plugins:android-apt:1.8'
    }
}
allprojects {
    repositories {
        jcenter()
    }
}
task clean(type: Delete) {
    delete rootProject.buildDir
}
``````
add plugin
``````
apply plugin: 'com.neenbedankt.android-apt'
``````
add deps
``````
compile 'com.jakewharton:butterknife:8.0.1'
apt 'com.jakewharton:butterknife-compiler:8.0.1'
``````
