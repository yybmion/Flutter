## 자식 위젯이 부모 위젯의 state를 사용하고 싶으면
___

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(
      MaterialApp(
          home : MyApp()
      )
  );
}

class MyApp extends StatefulWidget {
   MyApp({Key? key}) : super(key: key);

  @override
  State<MyApp> createState() => _MyAppState();
}

class _MyAppState extends State<MyApp> {
  var a =1;
  var name=['김영숙','홍길동','피자집'];

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(),
      body: ListView.builder(
        itemCount: 3,
        itemBuilder: (c,i){
          return ListTile(
            leading: Image.asset(('contact-people.png'),width: 100,),
            title: Text(name[i])
          );
        }
      ),
      floatingActionButton: FloatingActionButton(
        child: Text('버튼'),
        onPressed: (){
          showDialog(context: context, builder: (context){
            return DialogUI();
          });
        },
      ),
    );
  }
}

class DialogUI extends StatelessWidget {
  const DialogUI({Key? key}) : super(key: key);
  @override
  Widget build(BuildContext context) {
    return Dialog(
      child: SizedBox(
        width: 300,
        height: 300,
        child: Column(
          children: [
            TextField(),
            TextButton(child: Text('완료'), onPressed: (){}),
            TextButton(child: Text('취소'), onPressed: (){
              Navigator.pop(context);
            },)
          ],
        ),
      ),
    );
  }
}
```
![50](https://user-images.githubusercontent.com/113106136/215275740-35718966-e748-46fc-9563-85f84edbf014.png)


___

부모 변수를 자식에서도 사용하는 방법??
![53](https://user-images.githubusercontent.com/113106136/215275993-1e2a2be0-e92e-40b2-af2b-a594b720ce76.png)

1. 보내기 

2. 자식은 state 이름을 등록

3. 자식은 사용  
![51](https://user-images.githubusercontent.com/113106136/215275922-b6b99a5a-7d49-4218-9423-f86fa4f652b5.png)

![52](https://user-images.githubusercontent.com/113106136/215275923-dd4161ae-3cde-422c-bd9d-2fcbd03dd6d5.png)

참고) 부모 위젯 -> 자식 위젯 이렇게만 전송이 가능합니다.

자식 -> 부모 이런 식의 패륜 전송이나

서로 관련없는 옆집 위젯끼리의 불륜 전송은 어렵습니다. 

 

(교훈) 그래서 많은 위젯들이 사용해야하는 중요한 state는 최대한 위에 보관해주는게 좋습니다.

중요한 것들은 그냥 MyApp 이런데 넣으면 됩니다. 

___

## 사용자의 input을 받는 법

유저가 TextField()에 입력한 내용을 가져오고 싶다면 ??

```dart
class DialogUI extends StatelessWidget {
  DialogUI({Key? key, this.addOne }) : super(key: key);
  final addOne;
  var inputData = TextEditingController();
```
TextField() 위젯에 controller: 파라미터가 있습니다.

```dart
TextField(
  controller: inputData,
), 
```
