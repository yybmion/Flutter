## TextField에 스타일 주는 방법
___

> TextField 양옆에 아이콘 넣고 싶으면 icon: 파라미터 

```dart
TextField(
  decoration: InputDecoration(
    icon: Icon(Icons.star),
  ),
), 
```
![62](https://user-images.githubusercontent.com/113106136/215935908-bcf65a17-0f68-4088-8d79-f9ac6c712f43.png)

icon: 파라미터 대신

prefixIcon:

suffixIcon:

이런 파라미터도 있습니다.

> border 주려면 enabledBorder: 파라미터

```dart
TextField(
  decoration: InputDecoration(

    enabledBorder: OutlineInputBorder(
      borderSide: BorderSide(
        color: Colors.green,
        width: 1.0,
      ),
    ),

  ),
),
```
![63](https://user-images.githubusercontent.com/113106136/215936243-9c6d70d3-1863-4c06-8ccc-84f9b2ea24b2.png)


커서찍혔을 때, 에러일 때 등 테두리를 변경하고 싶으면 enabledBorder: 뿐만 아니라 

border:

focusedBorder:

disabledBorder:

errorBorder:

focusedErrorBorder:

이런 파라미터를 더 넣어보시길 바랍니다. 

> border를 하단만 주려면 

```dart
TextField(
  decoration: InputDecoration(
    enabledBorder: UnderlineInputBorder(),
  ),
), 
```
![64](https://user-images.githubusercontent.com/113106136/215936304-b7e9da05-7426-46cb-ba63-1bb56b6e96f0.png)

OutlineInputBorder() 위젯은 상하좌우 테두리를 주고 

UnderlineInputBorder() 위젯은 하단 테두리만 주고

InputBorder.none 위젯 쓰면 테두리를 없애줍니다. 

이 위젯들 안에서 border 두께, 색상 이런거 커스터마이징하면 됩니다. 

언제나 자동완성을 활용합시다. 

> 테두리 둥글게 하고 싶으면 borderRadius :

```dart
TextField(
  decoration: InputDecoration(

    enabledBorder: OutlineInputBorder(
      borderRadius: BorderRadius.circular(30),
    ),

  ),
), 
```
![65](https://user-images.githubusercontent.com/113106136/215936469-c27b0d75-bf50-43b8-a3ea-ffb4441795ea.png)


> border 없애기 & 배경색 입히기

```dart
TextField(
  decoration: InputDecoration(

    filled: true,
    fillColor: Colors.blue.shade100,
    enabledBorder: OutlineInputBorder(
      borderSide: BorderSide.none,
    )

  ),
), 
```

borderSide: BorderSide.none 이건 테두리 선을 없애줍니다. 

![66](https://user-images.githubusercontent.com/113106136/215936588-0c5d9d83-d5d0-47ba-8773-3fc4dbc5f025.png)

> 근처에 힌트 띄우고 싶으면

```dart
TextField(
  decoration: InputDecoration(
    hintText: 'hint',
    helperText: 'helper',
    labelText: 'label',
    counterText: 'counter'
  ),
), 
```

![67](https://user-images.githubusercontent.com/113106136/215936715-84474a88-fdb9-4556-b389-9c3859410b2a.png)

4개 중 원하는 것만 고르면 됩니다.

이 글자들 스타일주고 싶으면 

hintStyle: TextStyle(color: Colors.green), 

이런 파라미터를 더해주면 됩니다. 

