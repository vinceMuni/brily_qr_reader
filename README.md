# flutter_qr_reader

QR code (scan code &#x2F; picture) recognition （AndroidView&#x2F;UiKitView）

## DEMO

![demo](https://github.com/hetian9288/flutter_qr_reader/blob/master/Screenshot_20190608-153849.jpg?raw=true)

![demo](https://github.com/hetian9288/flutter_qr_reader/blob/master/ezgif-3-7c8bfe5fd68a.gif?raw=true)

## Getting Started

``` dart
import 'package:flutter_qr_reader/flutter_qr_reader.dart';
```


## Built-in UI

``` dart
Widget build(BuildContext context) {
    return new Scaffold(
      body: QrcodeReaderView(onScan: onScan),
    );
}

Future onScan(String data) async {
    await showCupertinoDialog(
      context: context,
      builder: (context) {
        return CupertinoAlertDialog(
          title: Text("扫码结果"),
          content: Text(data),
          actions: <Widget>[
            CupertinoDialogAction(
              child: Text("确认"),
              onPressed: () => Navigator.pop(context),
            )
          ],
        );
      },
    );
}
```