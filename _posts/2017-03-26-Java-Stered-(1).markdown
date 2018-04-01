---
layout: post
title:  "자바 시작하기 (1)"
date:   2018-03-27
image: "https://user-images.githubusercontent.com/15180507/37905760-d8aa7656-313a-11e8-8a85-77edba3d312b.png"
---

# Java란?

- - -

Java는 1995년에 개발되어 이제는 좀 연세가 되신 프로그래밍 언어이다.<br>이 Java는 객체지향언어를 지향하는 언어이며, 나름 생산성이 좋은 편에 속하는 언어이다.<br>다수의 초보 개발자들이 객체지향의 의미를 이해하지 못하고 프로그래밍을 그만두게 만드나, 이 객체지향의 뜻을 이해하면 프로그램을 만들때 상당히 수월히 만들수가 있게 된다는 장점이 있다.

## Java프로그래밍 전 준비 작업

- - -

- JDK(Java Develop Kit) 설치
- Java 환경변수 설정
- Java IDE(Eclipes) 설치

## JDK(Java Develop Kit) 설치

- - -

- Google 검색창에 JDK를 입력하면 Java JDK 최신판을 설치하는 페이지가 나온다(여기)![ JDK(Java Develop Kit) 설치-1](https://user-images.githubusercontent.com/15180507/37904792-c0cf44ba-3137-11e8-95fd-1cedb5d3a8b2.png)

- 그 후 제일 위에있는 Java SE Development Kit창에서  Accept License Agreement 버튼을 클릭한다![ JDK(Java Develop Kit) 설치-2](https://user-images.githubusercontent.com/15180507/37904900-12ef49d4-3138-11e8-85e8-ec761c3cf793.png)

- 이제 JDK를 다운로드를 받아야 되는데 이를 위해서는 현재 컴퓨터의 사양을 알아야 한다. 컴퓨터의 사양을 알아보는 포스트다<br>(나 같은 경우는 윈도우 64비트 이므로 Window x64옆에 있는 파일을 다운 받겠다)![ JDK(Java Develop Kit) 설치-3](https://user-images.githubusercontent.com/15180507/37904933-2ea1df48-3138-11e8-9b75-1b60be8a4f19.png)

- 다운로드가 끝나면 설치파일을 실행을 하면 되는데 그부분은 생략하겠다

## Java 환경변수 설정

- - -

- 내컴퓨터(오른쪽 클릭) - > 속성 에 들어가시면 고급 시스템 설정이 있습니다 여기에 들어 갑시다.<br>![ Java 환경변수 설정-1](https://user-images.githubusercontent.com/15180507/37905051-91425c7c-3138-11e8-85e5-68d3b264d995.png)

- 시스템 속성차이 뜨면 고급탭에 들어가시면 환경변수가 있습니다. 이 환경변수는 나중에 Cmd창에서 Java를 직접적으로 실행을 할 때 사용되는 것으로 이부분이 제대로 되있지 않을경우 차후에 Eclipes를 시작시 오류가 나올 수 있습니다.<br>![ Java 환경변수 설정-2](https://user-images.githubusercontent.com/15180507/37905065-9c3078ee-3138-11e8-9317-283a1bc117a3.png)

- 환경변수가 뜨면 사용자 변수부분과 시스템 변수가 있는데 사용자 변수는 현재 컴퓨터를 사용하는 유저에게만 적용이 되는변수이고 시스템 변수는 컴퓨터를 사용하는 모든 유저에세 적용이 되는 변수이나 적용은 재부팅을 한뒤에 적용이 된다. 일단 빠른 설치를 위해 사용자 변수에 환경변수를 추가를 할것이다.<br>![ Java 환경변수 설정-3](https://user-images.githubusercontent.com/15180507/37905232-291b37d0-3139-11e8-84b4-5f71e3ce739d.png)

- JDK를 설치할때 경로를 변경하지 않으신 분들은 Java파일이 C:\Program Files\Java 내부에 있을것이다 이중 jdk로 시작하는 파일에 들어가서 주소창을 복사하자<br>![ Java 환경변수 설정-4](https://user-images.githubusercontent.com/15180507/37905247-353e709a-3139-11e8-87f6-b8dc79cfd974.png)

- 환경변수 창으로 다시 돌아와서 새로 만들기를 누르고 변수 이름 부분에  JAVA_HOME 을 입력하고 변수값에는 방금 복사한 주소를 붙여 넣자. <br>(이와 같은 식으로 변수 이름 부분에 CLASS_PATH를 넣어주고 변수 값부분에는 %JAVA_HOME%\bin\tools.jar 을 넣어주자)<br>![ Java 환경변수 설정-5](https://user-images.githubusercontent.com/15180507/37905333-787f48f2-3139-11e8-90a3-c014b68ddcad.png)

- 마지막으로 Path변수가 있을터인데 Path 변수를 클릭후 편집을 눌러주자 그러면 변수 값에 값들이 있을터인데 그 값들은 건들이지 말고 값의 끝- 부분에 ;(세미콜론)을 추가 해주고 %JAVA_HOME%\bin;을 추가해주면 된다.<br>![ Java 환경변수 설정-6](https://user-images.githubusercontent.com/15180507/37905368-98d9d306-3139-11e8-8982-2d1eee58c81d.png)

- 이제 제대로 환경변수가 되었는지 확인을 해야되는데 방법은 Cmd창에 javac -version을 쳐보자 찾을 수 없는 명령이라고 나오면 환경변수 설정이 잘못된 것이니 경로나 변수 이름이 잘못되었는지 확인을 해보자<br>![ Java 환경변수 설정-7](https://user-images.githubusercontent.com/15180507/37905383-ab59e002-3139-11e8-89d1-c64d1e94aa5b.png)

## Java IDE(Eclipse) 설치

- - -

- https://www.eclipse.org/ 이곳에 들어가면 Eclipse 설치 페이지가 나온는데 오른쪽 위에 Download버튼이 있으니 누르자<br>![ Java IDE(Eclipse) 설치-1](https://user-images.githubusercontent.com/15180507/37906277-80b197c0-313c-11e8-9fbc-234b3f784ff3.PNG)


- 그러면 DOWNLOAD 64BIT 또는 DOWNLOAD 64BIT가 있다 누르면 다운로드가 시작된다.<br>![ Java IDE(Eclipse) 설치-1](https://user-images.githubusercontent.com/15180507/37905445-e800a7fc-3139-11e8-998a-0c39d2fffacf.png)

- 다운을 다 받고 실행을 하면 eclipse Installer 가 뜨는데 선택창이 나오면 Eclipse IDE for Java Developers를 선택하자<br>![ Java IDE(Eclipse) 설치-1](https://user-images.githubusercontent.com/15180507/37905452-ecc35f46-3139-11e8-8329-48972fad8d16.png)

- 경로를 지정하는 창이 나오면 그냥 무시하고 INSTALL을 누르면 설치가 시작된다<br>![ Java IDE(Eclipse) 설치-1](https://user-images.githubusercontent.com/15180507/37905463-f2cc4ef2-3139-11e8-8426-a9fcc3ff643e.png)

이로서 Java를 이용하여 프로그래밍을 하기위한 환경설정이 끝났다. 이 다음 포스트에서는 자바의 기본적인 구조를 설명하고 프로그래밍의 시작점인 "Hello World!"출력하기를 해볼것이다