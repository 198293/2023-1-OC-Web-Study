# 2023-1-OC-Web-Study

2주차 (03/21) WIL입니다.
https://bloom-channel-2ab.notion.site/WIL2-a592d6bd4abc457283751da01134bd06

# WIL2

Weekly I learned Week 2

1주차 + 2주차 복습

마감기한 2023년 03월 28일 03:00

# 1주차

## 서버(Server)

**→ 클라이언트에게 네트워크를 통해 서비스하는 컴퓨터 (== 제공자)**

**→ 실제 인터넷은 수많은 서버, 라우터 등이 거미줄 처럼 얽혀서 형성된 것**

**→ 서비스의 규모가 커질수록 서버의 규모도 커진다. (데이터 센터의 존재 이유이기도 하다.)**

## 리소스(Resource)

**→ 시스템에서 작업을 수행하는 실질적이나 가상의 장치나 요소 등의 자원 (ex : 프린터, 디스크 드라이브, 메모리 등)**

**→ 운영체제에서 리소스는, 프로그램들이 활용할 수 있는 데이터나 루틴을 말한다.** 

**== 시스템 리소스**

## URL(Uniform Resource Locator)

**→ 인터넷에서 웹 페이지, 이미지, 비디오 등 리소스의 위치를 가리키는 문자열**

**→ HTTP 에서 URL은 웹 주소, 혹은 링크라고 불린다.**

**→ URL = 프로토콜 + 도메인 이름 + 포트 + 리소스 경로 + 추가 파라미터 + 부분 식별자**

## **DNS(Domain Name System)**

**→ 사람이 읽을 수 있는 도메인 이름을 실제 네트워크 상에서 사용하는 IP 주소로 변환하고 해당 IP주소로 접속하는 전반적인 시스템.**

**→ DNS는 전세계적으로 약속되어있다.**

**→ DNS = Domain Name Space + Name Server + Resolver**

 ****

**Domain Name Space = DNS를 Domain Name Space라는 규칙으로 도메인 이름 저장을 분산한다.**

**Name Server = 권한 있는 DNS 서버**

**Resolver = 권한 없는 DNS 서버**

# 2주차

## Git이란?

> **→ "Git : The Information Manager from Hell"**
> 

**→ 코드의 분기를 만들고 합치는 것이 가능하다. 이때 분기는 branch라 한다**

**→ 코드의 변화를 추적하고,  임의대로 일정 갯수의 변화들을 모아 저장할 수 있다.**

### Git에서 파일의 네 가지 상태

![img1.daumcdn.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2c40a2be-27ad-4236-b8b5-0867af783152/img1.daumcdn.png)

1. **추적하지 않는 상태 (untracked)**
2. **추적하지만 변경이 없는 상태 (unmodified)**
3. **변경이 있는 상태 (modified)**
4. **Staged 상태 (staged)**

![img1.daumcdn.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7f147f05-c22b-490b-bafc-61614a868bcd/img1.daumcdn.png)

### Working directory

**→ 사용자의 작업 공간으로, 실제 파일을 수정하거나 생성하는 공간**

**→ Working directory에서는 파일들은 tracked/untracked 상태로 구분한다.**

**Tracked 상태**

**→ git에 의해서 파일의 변경 이력이 추적된다.**

**→ 모든 파일의 변경 이력을 추적한다면 시스템의 부하가 커지기 때문에 git에서 요청받은 파일들만 변경 이력을 추적한다.**

**→ 명령어 $git add <file.name> ⇒ 이름이 <file.name>인 파일을 stage 영역으로 등록시킨다.**

**Untracked 상태**

**→ 저장소 내에서 새로 만들어진 모든 파일들은 untracked 상태로 시작한다.**

**→ Untracked 상태인 저장소 내의 파일들은 git이 코드 변경이력을 추적하지 않는다.**

### Staging area

→ **변화들을 쌓아놓는 공간, 중간저장소**

**→ Tracked 상태의 파일들을 관리 및 임시로 저장하는 공간**

→  **staging영역에 변화들을 쌓을 때는 git add 명령어를 사용한다. (앞에서 언급)**

**→ 파일의 콘텐츠 내용을 직접 가지고 있는 것이 아닌, commit하려는 파일의 추적 상태 정보들만 기록한다.**

→ 내 PC에 파일이 저장되는 개인 전용 로컬의 git 저장 ⇒ 내 PC에 위치한 git 설정된 디렛토

### **local repository**

→ **Staging area에 있는 변화들은 commit 명령어를 통해 local repository로 이동한다**

### Remote repository

**→ git의 변화 데이터들을 모아둘 수 있는 곳**

**→ 파일이 원격 저장소 전용 서버에서 관리되며 여러 사람이 함께 공유하기 위한 저장소 == 공통의 외부 저장소** 

**→ Github가 이 remote repository에 해당한다.**

→ **FETCH와 PULL을 통해 타인의 코드를 받고, push를 통해 커밋한 내용을 remote repository에 밀어 넣을 수 있다.**

## **Github란?**

**→ Remote repository 중 하나**

**→ 버전 관리와 협업을 위한 코드 웹 호스팅 플랫폼 ⇒ Git을 더 쉽고 간편하게 사용할 수 있다.**


###

1주차

서버 → [https://contents.premium.naver.com/3mit/wony/contents/220117230634163vp](https://contents.premium.naver.com/3mit/wony/contents/220117230634163vp)

[https://developer.mozilla.org/ko/docs/Learn/Common_questions/Web_mechanics/What_is_a_web_server](https://developer.mozilla.org/ko/docs/Learn/Common_questions/Web_mechanics/What_is_a_web_server)

리소스→ [https://codebreaking.tistory.com/74](https://codebreaking.tistory.com/74)

[https://gunggum2.tistory.com/150](https://gunggum2.tistory.com/150)

URL→ [https://developer.mozilla.org/ko/docs/Glossary/URL](https://developer.mozilla.org/ko/docs/Glossary/URL)

[https://developer.mozilla.org/ko/docs/Learn/Common_questions/Web_mechanics/What_is_a_URL](https://developer.mozilla.org/ko/docs/Learn/Common_questions/Web_mechanics/What_is_a_URL)

DNS→[https://hanamon.kr/dns란-도메인-네임-시스템-개념부터-작동-방식까지/](https://hanamon.kr/dns%EB%9E%80-%EB%8F%84%EB%A9%94%EC%9D%B8-%EB%84%A4%EC%9E%84-%EC%8B%9C%EC%8A%A4%ED%85%9C-%EA%B0%9C%EB%85%90%EB%B6%80%ED%84%B0-%EC%9E%91%EB%8F%99-%EB%B0%A9%EC%8B%9D%EA%B9%8C%EC%A7%80/)

2주차

→ Git의 유래와 개념, 기본 동작 원리, 간단한 사용법

[https://dwaejinho.tistory.com/entry/GIT-GitThe-Information-Manager-from-Hell-깃과-깃허브](https://dwaejinho.tistory.com/entry/GIT-GitThe-Information-Manager-from-Hell-%EA%B9%83%EA%B3%BC-%EA%B9%83%ED%97%88%EB%B8%8C)[https://dwaejinho.tistory.com/entry/Git-Git-file-status-lifecycle#](https://dwaejinho.tistory.com/entry/Git-Git-file-status-lifecycle#)

[https://m31phy.tistory.com/146](https://m31phy.tistory.com/146)

[https://nemomemo.tistory.com/75](https://nemomemo.tistory.com/75)

[https://velog.io/@jini_eun/Github-Github란-간단-정리](https://velog.io/@jini_eun/Github-Github%EB%9E%80-%EA%B0%84%EB%8B%A8-%EC%A0%95%EB%A6%AC)

 선택 과제 다시 해보기

[https://www.youtube.com/watch?v=ZQg73e1KLfo](https://www.youtube.com/watch?v=ZQg73e1KLfo)

[https://wadekang.tistory.com/25](https://wadekang.tistory.com/25)


