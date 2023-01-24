## ListView.builder
___

H.W 내 답
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
        appBar: AppBar(title: Text('연락처'),toolbarTextStyle: TextStyle(color: Colors.green,letterSpacing: 7)),
        body: Container(
          child: Column(
            children: [
              contact(),
              contact(),
              contact(),
            ],
          ),
        ),
        bottomNavigationBar: BottomAppBar(
          child: widget1(),
        ),
        )
      );
  }
}


class widget1 extends StatelessWidget {
  const widget1({Key? key}) : super(key: key);

  @override
  build(BuildContext context) {
    return BottomAppBar(
      child: Row(
        mainAxisAlignment: MainAxisAlignment.spaceEvenly,
        children: [
                Icon(Icons.phone),
                Icon(Icons.message),
                Icon(Icons.contact_page),
              ],
      )
    );

  }
}

class contact extends StatelessWidget {
  const contact({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return Container(
      padding: EdgeInsets.all(10),
      child: Row(
        children: [
          Image.asset('contact-people.png',width: 40,),
          Text('홍길동',style: TextStyle(letterSpacing: 7)),
        ],
      ),
    );
  }
}
```
결과

![33](https://user-images.githubusercontent.com/113106136/214310962-3105dd8c-1bff-412b-a3cc-4bd9a667f00d.png)

ListTile은 쉽게 그림 옆에 글 같은 꼴을 쉽게 만들어줌

ListView 를 통해 반복문을 만들어보자
![35](https://user-images.githubusercontent.com/113106136/214312408-588bbfb7-0519-49af-8a7d-519c5326b62b.png)

![34](https://user-images.githubusercontent.com/113106136/214312434-3ac66bf4-2218-48f4-9ca7-9b6b9a9f0474.png)

![36](https://user-images.githubusercontent.com/113106136/214313414-e29acf92-0ef2-4076-a41f-ce241e8513ce.png)

![37](https://user-images.githubusercontent.com/113106136/214313436-4726be27-b6b5-41d8-84f4-f09c0407ebef.png)

___

버튼 기능
![38](https://user-images.githubusercontent.com/113106136/214314393-bd283179-bb84-41ec-97ce-0c4d5c7468d6.png)

버튼을 누를 때 마다 1씩 증가하는 프로그램을 만들어보자!

![39](https://user-images.githubusercontent.com/113106136/214314567-0a2b2fd5-38cb-47eb-ad5e-991a1aa06c90.png)
![40](https://user-images.githubusercontent.com/113106136/214314682-7cf6d5c6-16fb-43dd-a586-4bc1ff198515.png)

증가하는것을 볼 수 있다.

___
![41](https://user-images.githubusercontent.com/113106136/214316678-cb9f71f2-2558-45a8-b704-a952a0db4ffe.png)

![42](https://user-images.githubusercontent.com/113106136/214316792-a202c6fe-0b3a-4c85-8287-af9981b9095d.png)

아니 누를 때 마다 왜 증가 안함?

콘솔 창에서는 증가하지만 화면해서는 증가가 안한다

그 이유는 렌더링이 안돼서그렇다.

자동으로 재렌더링을 하려면 STATE를 써준다.

state 만드는 법
1. statefulWidget 만들기
2. 거기 둘 째 clss 안에 변수만들기

**중요**!!!!

state 변경하려면
setState((){여기서}) 해야함

![43](https://user-images.githubusercontent.com/113106136/214318475-2b84a9dc-15ff-4569-96b6-0d15306b99f5.png)

![44](https://user-images.githubusercontent.com/113106136/214320079-773bd0f4-2d53-4d1f-8689-8cef8e8c7541.png)

![45](https://user-images.githubusercontent.com/113106136/214320092-3ad1e3a5-7414-4876-b2ed-ea4a815cd61f.png)

