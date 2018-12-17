# Learning Dart Language

## Introduction 

Learning Dart isn't a smooth ride when the documentation doesn't share much information or technically put, we are yet to understand the log printed.

## Why learn Dart?

Currently Dart is learned for only one admittable reason, to develop applications using [Flutter](https://flutter.io/) which is a "single code base" for Developing both Andriod and IOS application. If you are new to the Flutter Development which is very easy to do. Then the only thing that might become an hurdle is your less to No knowledge in Dart. 

So, to get started in Flutter, you have to learn Dart.

## What is Dart, to which i can compare it to?

Dart is an Runtime, Programming Language which is based on Object Oriented Concepts. Google felt Javascript is fundamentally flawed and believed a new programming language could solve the problems that javascript couldn't at that point of time. Google packaged Dart Runtime in Chrome Browser and made it available to be executed in the Browser directly as a Alternative to Javascript as how VBScript was used in the earlier days.

For Dart Web application to run in all the browsers, all the other Browser Vendors should also package Dart runtime, which never happened. Until the release of Dart 2.0(which is a major rewrite compared to its earlier Version), Developers used a custom build of Chromium Browser which is called **Dartium** for Development and the release version of the web application is transpiled to Javascript.

With Dart 2.0, This is not the case. Today, we use Chrome browser(doesn't contain Dart) for Development and release can be transpiled to Javascript, which will work in all Browser. What you are thinking is right, the development, debug can be done & will work only in the Chromium based Browsers. However, I have never tried development based on Opera, so it could be just Chrome.

To answer the question **to which i can compare it to?**, I think NodeJS is the right one to compare with.

### Why NodeJS?

Java is a runtime, so does the NodeJS. Why I believe that NodeJS can be compared to the Dart is because of the similarities and more than that you might feel that the Dart has handled some of the problems that has a Javascript Developer we might face in Javascript and NodeJS.

Lets look into some of the comparables in both

|Comparables|NodeJS|Dart|
|---|---|---|
|Single Threaded|Yes|Yes, but supports **isolate**, which is used in projects like Aqueduct|
|Packages|Tools developed are distributed as Packages, a Package can added as dependency or dev_dependency and used inside another package|Dart itself is a collection of packages, `dart:html`, `dart:io`, `dart:async` are the core packages of dart. both dependencies and dev_dependencies specification are available in Dart|
|Package specification file|`package.json` file contains all the information relating to the Project, this is not limited to Name, description, license but also list the dependencies and dev_dependencies. `scripts` contains the list of scripts that can be executed using the `npm run` command. `npm init` helps you in generating a simple `NodeJS` project with `package.json` file.|Dart uses `pubspec.yaml`, there is no scripts support. `pub run` is used instead.|
|Package Manager|`npm` or `yarn`. npm is bundled in NodeJS|`pub` is bundled in Dart and handles everything related to packages. `pub get` & `pub global activate` are the 2 commands used predominantly. Former for installing packages locally and later is for global.|
|packages download path|Global packages are store in the `npm` or `yarn` folder, whereas packages dependencies are store inside `node_modules` folder of the current package.|`pub` doesn't store the packages in the package folder, instead store `.packages` file, which contains all package dependencies along with the global pub cache path where it is available.|
|package lock|`package-lock.json` or `yarn.lock` handles locking of version of dependency packages.|`pubspec.lock` does the same job.|

## Scaffold a basic "Hello world" application

Use `Stagehand` package for scaffolding an basic dart application.

If your needs are different from the template list supported by `Stagehand` then you may have to search the [pub site](https://pub.dartlang.org). I have listed some of them that I know & remember.

1. `flutter create` - flutter provides the CLI tool for scaffolding an flutter application. use `fluttter doctor` to check whether your development environment supports development of Android and IOS.

2. `aqueduct create` - aqueduct provide the CLI tool for scaffolding an Aqueduct based Web Server that can connect with `Postgresql` DB.

3. `angular_cli` provides option to create Component, pipe, service for an AngularDart application which is scaffolded by using `Stagehand`. 

4. use `monorepo` package to hold all the different types of Dart applications in a single Repo.