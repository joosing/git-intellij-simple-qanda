**Q : 특정 경로에 있던 파일이 보이지 않아요? 실수로 삭제(또는 이동)된 것 같아요. 어느 커밋에서 삭제된 걸까요?**

A : git command line 을 활용해야 할 것 같아요. 다음을 따라해 봅니다.

> 1. 우선 삭제된 파일이 있었던 경로를 확인합니다. (Project > 디렉토리 우클릭 > Copy Path/Reference > Path From Content Root)

![](https://velog.velcdn.com/images/joosing/post/de27ad63-46e2-4873-ba19-77516dba36c8/image.png)

> 2. Intellij 에서 Terminal 윈도우를 엽니다. (Menu > Tool Windows > Terminal)

![](https://velog.velcdn.com/images/joosing/post/793e2f88-4a5d-4371-8059-7cb2857b8c9f/image.png)

> 3. 프로젝트 루트 경로에서 Terminal 이 열립니다.

![](https://velog.velcdn.com/images/joosing/post/53c7f2fd-90de-4ac5-b332-a391d77b00ea/image.png)

> 4. 다음 명령어를 위에서 찾은 경로와 함께 입력합니다. 경로는 상황에 따라 현재 디렉토리에서 상대경로로 입력하면 됩니다 ([명령어 상세 설명](https://git-scm.com/book/ko/v2/Git%EC%9D%98-%EA%B8%B0%EC%B4%88-%EC%BB%A4%EB%B0%8B-%ED%9E%88%EC%8A%A4%ED%86%A0%EB%A6%AC-%EC%A1%B0%ED%9A%8C%ED%95%98%EA%B8%B0))

```java
git log --name-status -- src/main/java/com/example/programming/test/MyTest.java
```
> 5. 다음과 같이 해당 파일의 이력만 따로 출력 됩니다. 엔터를 치면서 이력을 확인하며 D(Delete) 라고 표시된 커밋을 찾습니다.

![](https://velog.velcdn.com/images/joosing/post/db2841c3-4e3e-4520-ade8-e15621bc058c/image.png)

> 6. 해당 커밋의 해쉬 값을 복사하고 Q를 입력하여 log 확인 모드(?)에서 빠져나옵니다. 
> 7. 해당 커밋을 Revert 합니다. 아래와 같이 명령을 입력합니다.

```java
git revert 2154c61839bbb870c9cf8080986b82e067917da2 --no-edit
```

> 8. 삭제된 커밋이 되돌려집니다. 아래 예시는 .../test/MyTest.java 경로에 있던 파일이 .../pojo/MyTest.java 로 옮겨진 실수가 복구된 예시입니다. 

![](https://velog.velcdn.com/images/joosing/post/8ae83fee-0223-47aa-bcc7-70c9475f843a/image.png)
