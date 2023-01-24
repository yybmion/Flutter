## Dialog
___

들어가기 전 팁

왼쪽에 붙일 때는 leading 속성에, 오른쪽에 붙일 때는 trailing 속성에 위젯이나 아이콘을 달아주면 됩니다.

H.W

![46](https://user-images.githubusercontent.com/113106136/214326827-f50e7478-5dc9-467c-86d4-344200185225.png)
![47](https://user-images.githubusercontent.com/113106136/214326834-b4378c64-96d0-403c-9d23-1545d127011c.png)


![48](https://user-images.githubusercontent.com/113106136/214333128-32a31218-ebc1-462e-bc4c-1446f354b712.png)

근데 안뜨는데??

그럴때는 context는 족보인데 여기에 MaterialApp이 들어있어야 Dialog가 작동한다.

근데 만약 MaterialApp이 커스텀 클래스에 있으면 Context에 아무것도 없으니 MaterialApp은 위로 보내준다.

그러면 잘 작동할 것이다.

![49](https://user-images.githubusercontent.com/113106136/214333713-4439fa87-3687-48a6-a7fb-1823736c7195.png)
