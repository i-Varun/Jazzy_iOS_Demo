# Swift project documentation genetation using Jazzy

How to setup Jazzy ?

Open your Terminal from Dock and type following command:

```sh
[sudo] gem install jazzy
```
Set options for your project’s documentation in a configuration file, .jazzy.yaml by default. Create a .jazzy.yaml file using below command in Terminal.

```
touch .jazzy.yaml
```

Add below configuration in .jazzy.yaml file:

```
# Jazzy config
module: Jazzy_iOS_Demo
author: Varun Patel
swift_version: 5.3.2
xcodebuild_arguments: [clean,build,-workspace,Jazzy-iOS-Demo.xcworkspace,-scheme,Jazzy-iOS-Demo]
min_acl: private
theme: apple
output: 'Documentation/Jazzy_Demo'
use_safe_filenames: true

exclude: 
  - '*AppDelegate*'
  ```
Make sure you add correct module name in ```module```

All set now, open terminal type below command in terminal:

```
jazzy
```
You will see below outout in terminal:

```
Using config file /Volumes/Data/Development/GitHub Projects/Jazzy_iOS_Demo/.jazzy.yaml
Running xcodebuild
Parsing AppDelegate.swift (1/3)
Parsing SceneDelegate.swift (2/3)
Parsing ViewController.swift (3/3)
9% documentation coverage with 10 undocumented symbols
included 11 private, fileprivate, internal, public, or open symbols
building site
building search index
jam out ♪♫ to your fresh new docs in `Documentation/Jazzy_Demo`
```
Boom 🎇 ,Now open go to Documentation/Jazzy_Demo directory and open ```index.html```

