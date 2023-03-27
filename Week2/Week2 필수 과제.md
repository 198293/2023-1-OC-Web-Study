# 2023-1-OC-Web-Study
Web-Study Week2 필수 과제 제출

## **필수과제**
https://www.notion.so/2-4e1b85b8789948ee80d4d71cbce05d2a?pvs=4

**git의 명령어 add, commit, push는 각각 어떤 역할을 하는지 정리하고,
git pull과 fetch의 차이점을 정리하시오.**

### git add

**→ 작업 디렉토리 상의 변경 내용을 스테이지 영역에 추가하는 명령어**

**$ git add .** 

**현재 디렉토리의 모든 변경 내용을 스테이징 영역으로 넘기고 싶을 때 .을 인자로 사용한다.**

**$ git add -A**

**작업 디렉토리 내의 모든 변경 내용을 몽땅 스테이징 영역으로 넘기고 싶을 때 -A옵션 사용**

### **git commit**

**명시적으로 기록 남기기 == 의미 있는 변화에 대해 기록하는 것**

**→ 로컬 저장소에 코드 변경 이력을 남기기 위해서 사용된다.**

**→ 로컬 저장소에 많은 코드 변경 이력을 남기더라도 원격 저장소에서는 알 수 없기 때문에 git push 명령어를 사용해야 로컬 저장소에 남겨놓은 코드 변경 이력들이 원격 저장소로 전송된다.** 

→ **commit 기록은 git log 명령어를 통해 확인 가능하다.**

### **git push**

**→ 원격 저장소(Remote repository)에 코드 변경 이력을 업로드하기 위해서 사용하는 명령어**

→ **로컬 저장소에 남겨놓은 코드 변경 이력들이 원격 저장소로 전송된다. 사전에 add 명령어를 이용하여 원격 저장소와 내 로컬을 연결해야 한다.**

### **git pull**

**→ 원격 저장소에 있는 변경사항들을 로컬 저장소로 가져와 합치는 명령어**

**→ 원격 저장소에서 변경된 정보를 확인할 뿐만 아니라 최신 데이터를 복사하여 로컬 git에 가져온다.**

### **git fetch**

**→ 원격 저장소에 있는 변경 사항들을 로컬 저장소에 가져오기 전에 변경 내용을 확인하고 싶은 경우에 사용하는 명령어**

**→ 로컬 git 에게 원격 저장소에서 최신 정보를 확인하라는 명령을 전달한다. 변경된 데이터를 로컬 git에 실제로 가져오지는 않는다.**

### git pull과 git fetch의 차이점

→ **git pull의 경우 로컬 디렉토리에 변경 내용을 확인 및 병합하지만,** 

**pit fetch의 경우 변경 내용을 확인만 할 뿐 병합하지는 않는다.**




add  [https://www.daleseo.com/git-add/](https://www.daleseo.com/git-add/)

push  [https://www.daleseo.com/git-push/](https://www.daleseo.com/git-push/)

pull과 fetch [https://chaeyoung2.tistory.com/43](https://chaeyoung2.tistory.com/43)
