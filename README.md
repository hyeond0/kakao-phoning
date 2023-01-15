# Kokoa Project

## 노마드 10주 스터디 진행중!

23/01/02 ~ 23/01/15

https://hyeond0.github.io/kokoa-project/

노마드 코더 코코아톡 강의 졸업과제

### 컨셉

Y2K 컨셉을 디자인해서 만들 생각을 가지고 있다가 뉴진스의 Phoning 어플을 발견하고, 그 디자인을 클론해서 카톡 디자인과 결합시켜보았다.

### 프로젝트 만들면서 어려웠던 점 정리

- 페이지마다 배경화면의 색을 변경하고 싶었는데 css 자체에선 어떻게 해야할지 잘 몰랐었다.

  -> 배경화면은 우선 직접 만든 것이 아닌 인터넷에서 이미지 파일을 받아서 사용했다.
  css가 cascading인걸 이용해서 external css 파일 말고 html에 따로 <styles>를 만들어 배경화면을 페이지마다 바꿀 수 있도록 설정했다.
  -> html 파일에 styles를 만들어서 했다가, 각 html 파일의 body에 class를 주어 css 파일만으로 해당 화면마다 다른 배경화면이 나올 수 있도록 설정했다.

- nav bar에서 버튼을 직접 만들어 보려 했는데 마음에 들게 나오지 않아서 직접 이미지를 따와야 할지 고민하는 과정이나,
  아이폰 이모지를 쓰고싶은데 html 이모지는 이쁘지 않을 때..
  
  -> 이모지는 인터넷에서 img 파일 주소 복사를 사용했고, nav-bar 아이콘은 직접 핸드폰에서 어플을 캡쳐해서 누끼따는 작업을 통해 만들었다.

- alt-header 대신 채팅 스크린 전용 헤더를 따로 만들었는데, width:100%와 box-sizing: border-box를 사용해도 생각처럼 잘 정렬되지 않았다.

  → 숨겨둔 margin을 찾지 못해서 발생한 일이였다. width와 height를 조절할 때는 margin, padding을 잘 고려하면서 만들자.

- 배경화면 이미지가 gradient인데, 맨 위 screen-header 뿐 아니라 채팅스크린의 chat-header까지 같이 fixed를 하다 보니 배경화면을 설정하는 부분에서 색상을 어떻게 해야 할지 고민이 됐다.
  background:inherit을 사용하면 gradient로 밝아지다가 다시 진해지는 느낌이 나서 맘에 들지 않았다.
  background-color:inherit을 사용하면 부드럽게 밝아지는 느낌이 나지만 화면을 내리면 하얀 부분일 때 화면이 잘 가려지지 않는 문제가 발생했다.
  -> inherit을 안쓰고 직접 rgb 값 설정도 해보았는데, 밝아졌다가 다시 어두워지는 부분이 조금씩 보여 마음에 들지 않아 결국 inherit가 제일 티가 나지 않는 노란색을 사용했다.

- 채팅 화면에 어떤 내용을 넣을지 고민하다가 노래가사를 파트별로 나눠 넣기로 했는데, 한 파트당 노래 가사가 긴 만큼 줄 관리가 힘든 부분이 있었다.
  -> width를 조정해야 하나 고민했는데, 강제로 줄바꿈 시켜주는 <br/>을 알게 되어 쉽게 해결했다.
  하지만 br을 사용하다보니 줄 간격이 너무 좁게 느껴졌고, br을 2번 쓰면 너무 행간이 넓은 느낌이였는데 찾아보다가 line-height를 알게 되어 알맞게 조절했다.
