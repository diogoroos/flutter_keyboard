# flutter_keyboard

[![pub package](https://img.shields.io/pub/v/fl_numeric_keyboard.svg?style=for-the-badge&color=blue)](https://pub.dartlang.org/packages/flutter_keyboard)

Easily display a numeric keypad like those found on P.O.S (P.D.V in Brazil) equipment. Works on Android, iOS, Web, Windows, Linux and Mac.<br/>
Cloned and improved from the numeric_keyboard package.

## Installation

Add `flutter_keyboard: ^2.0.0` in your `pubspec.yaml` dependencies. And import it:

```dart
import 'package:flutter_keyboard/flutter_keyboard.dart';
```

## How to use

Simply create a `FlutterKeyboard` widget and pass the required params:

```dart
FlutterKeyboard(
  onKeyboardTap: _onKeyboardTap
)

_onKeyboardTap(String value) {
  setState(() {
    text = text + value;
  });
}
```

## Params

```dart
FlutterKeyboard(
  onKeyboardTap: _onKeyboardTap,
  characters: const ['1', '2', '3', 'A', 'B', 'C', '!', '@', '#'],
  footerMiddleCharacter: '💡',
  itemsPerRow: 3,
  getAllSpace: true,
  externalPaddingButtons: const EdgeInsets.all(12),
  buttonsDecoration: BoxDecoration(
    borderRadius: BorderRadius.circular(12),
    color: Colors.blue,
  ),
  footerRightAction: () {
    setState(() {
      textCtrl.text = textCtrl.text.substring(0, textCtrl.text.length - 1);
    });
  },
  footerRightChild: Container(
    alignment: Alignment.center,
    width: 50,
    height: 50,
    child: const Icon(Icons.backspace),
  ),
),
)
```

For a more detail example please take a look at the `example` folder.

## Example

Flutter keyboard:

<img src="https://raw.githubusercontent.com/huextrat/fl_numeric_keyboard/master/example/screenshot.png" width="400" height="790">

## -

If something is missing, feel free to open a ticket or contribute!
