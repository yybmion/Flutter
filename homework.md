```dart
import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}
class MyApp extends StatelessWidget {
  const MyApp({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(),
        body: Container(
          height: 150,
          padding: EdgeInsets.all(10),
          child: Row(
            children: [
              Image.asset('flutter-logo-sharing.png',width: 300,),
              Container(
                width: 300,
                child: Column(
                  crossAxisAlignment: CrossAxisAlignment.start,
                  children: [
                    Text('카메라팝니다'),
                    Text('금호동 3가'),
                    Text('7000원'),
                    Row(
                      mainAxisAlignment: MainAxisAlignment.end,
                      children: [
                        Icon(Icons.favorite),
                        Text('4'),
                      ],
                    )

                  ],
              )
              )
            ],
          ),
        ),
        )
      );
  }
}
```
![28](https://user-images.githubusercontent.com/113106136/213482486-9ecd34cc-0f88-4a84-9282-b674ae5a83db.png)

