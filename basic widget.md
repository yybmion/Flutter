### basic widgets
___

처음에는 main밑에 stless 적은후 tab키를 누른다.

![20230119_211356](https://user-images.githubusercontent.com/113106136/213440541-fe59b641-2507-4db5-bb84-3875f7d4bf12.png)

본격적으로 위젯을 만들어보자

위젯은
1. 글자위젯
2. 이미지위젯
3. 아이콘위젯
4. 박스위젯

___

글자위젯
```dart
class MyApp extends StatelessWidget {
  const MyApp({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Text('안녕')
    );
  }
}
```
아이콘위젯
```dart
class MyApp extends StatelessWidget {
  const MyApp({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Icon(Icons.shop)
    );
  }
}
```

이미지위젯
먼저 pubspec.yaml 파일에서 만든 디렉토리의 이미지를 모두 허용해준다고 설정해준다.
```dart
class MyApp extends StatelessWidget {
  const MyApp({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Image.asset("flutter-logo-sharing.png")
    );
  }
}
```
박스위젯
```dart
class MyApp extends StatelessWidget {
  const MyApp({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Center(
        child: Container(width:50,height:50,color: Colors.blue)
      )
    );
  }
}
```
