# SKAlertDialog
 
A library that walks a user through multiple on-boarding screens in a simple and easy way
  
 [![Flutter](https://img.shields.io/badge/Platform-Flutter-blue.svg)](https://flutter.dev/)
 [![pub package](https://img.shields.io/badge/pub-1.0.0-blueviolet.svg)](https://pub.dev/packages/status_alert)
 
## GIF

<p align="left">
  <img src="https://user-images.githubusercontent.com/10756609/74606492-cecdeb80-50f6-11ea-9cdb-a4497a718dc8.gif" width=“”400px” height="400px">
</p>

## 💻 Installation

You just need to add `sk_alert_dialog` as a [dependency in your pubspec.yaml file.](https://flutter.dev/docs/development/packages-and-plugins/using-packages)

```yaml
dependencies:
sk_alert_dialog: ^1.0.0
```

## Usage

### Import this class

```dart
import 'package:sk_alert_dialog/sk_alert_dialog.dart';
```

## Simple Alert

```dart
     SKAlertDialog.show(
        context: context,
        type: SKAlertType.info,
        title: 'Simple Alert',
        message: 'Hi! Welcome to SKALertDialog',
        onOkBtnTap: (value) {
          print('Okay Button Tapped');
        },
      );
```
### Pass it into SKOnboardingScreen Widget

```dart
  @override
  Widget build(BuildContext context) {
    // TODO: implement build
    return Scaffold(
      body: SKOnboardingScreen(
        bgColor: Colors.white,
        themeColor: const Color(0xFFf74269),
        pages: pages,
        skipClicked: (value) {
          print("Skip");
        },
        getStartedClicked: (value) {
          print("Get Started");
        },
      ),
    );
  }
```

## 📃License

    Copyright 2020, Senthil Kumar

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
