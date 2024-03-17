Image Field 만들기
===================

Pitture URL이라는 이미지 링크가 저장되어 있는 Field를 만들어줍시다.

이 Field는 Text 데이터를 가지고 있습니다.

Field를 새로 만들어줍시다.   

데이터 타입은 Formula로 지정.

![스크린샷 2024-03-17 오후 10 55 17](https://github.com/pursWon/CRM101/assets/99719661/b73d2e53-a39f-49d4-ab1a-68fa41c4946d)

</br>

Label의 이름을 지정.

![스크린샷 2024-03-17 오후 10 53 53](https://github.com/pursWon/CRM101/assets/99719661/05efdead-19d9-4ae9-a064-e87697b11ffb)

</br>

Return Type은 Text로 지정해줍시다.

![스크린샷 2024-03-17 오후 10 56 45](https://github.com/pursWon/CRM101/assets/99719661/59055808-7f92-454f-b65f-fdff487d8a62)

</br>

Formula의 내용은 다음과 같습니다.

IMAGE (Picture_URL_c, "Contact Image", 200, 200)

-> 첫번째는 Image 링크가 담겨있는 필드의 이름    

두번째는 만들고 있는 필드의 이름

앞의 200은 Width, 뒤의 200은 Height를 의미합니다.

</br>

![스크린샷 2024-03-17 오후 10 57 42](https://github.com/pursWon/CRM101/assets/99719661/64c1dbbe-74e1-4f6c-aea5-94af128558ae)

</br>

만든 필드는 Page layout에 가서 보여주고 싶은 위치에 옮겨주면 이제 링크에 해당되는 이미지를 

해당 Object의 Record를 눌렀을 때 볼 수 있습니다!

![스크린샷 2024-03-17 오후 11 05 45](https://github.com/pursWon/CRM101/assets/99719661/48c51d49-320b-4850-a465-ee59f5a4d2aa)

</br>

아래와 같이 출력됨.

![스크린샷 2024-03-17 오후 11 07 39](https://github.com/pursWon/CRM101/assets/99719661/af2d1fda-32ff-4613-a02f-e2a7f97a100b)




