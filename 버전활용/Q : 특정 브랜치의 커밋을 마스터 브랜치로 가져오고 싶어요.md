> 이 기능은 조금 자세히 원리와 함께 정리합니다. 

# Problem-Case

어제 병합한지 오래된 master 브랜치에서 과거의 특정 버그수정 내용만 가져와야 할 일이 있었습니다. 두 브랜치는 고객이 달라져 별도로 관리하는 바람에 이제 머지가 거의 불가능한 수준이 되어서 꼭 필요한 버그수정 커밋만 가져와 충돌을 최소화해야 했습니다.

# Cherry-Pick

우리에게 꼭 맞는 기능이 Git 의 Cherry-Pick 이라는 기능이었는데요. 사용방법을 설명하기 앞에 Cherry-Pick 기능의 대략적인 개념정리가 먼저 필요한 것 같습니다. Cherry-Pick 기능은 아래 그림에서 보는 것 처럼 소스 브랜치의 일부 커밋(Cherry)을 선택(Pick)해서 타겟 브랜치의 헤드 위치로 옮겨 올 수 있는 기능입니다. 이 때 소스 브랜치가 변경사항을 제공하는 브랜치가 되겠고, 타겟 브랜치가 변경사항을 적용할 브랜치가 되겠습니다. Cherry-Pick 을 수행하려면 먼저 타겟 브랜치로 체크아웃한 상태에서 소스 브랜치의 커밋 히스토리를 보며 가져올(Pick) 커밋(Cherry)을 선택하는 작업을 해야합니다. 

![](https://velog.velcdn.com/images/joosing/post/133008b6-45da-4f5d-b9da-05dc1d8ed3a5/image.png)

# How-To

다음은 IntelliJ 에서 제공하는 Git GUI 를 통해 Cherry-Pick 을 수행하는 과정을 정리해 보았습니다. 관련된 기본적인 Git Command Line 명령도 함께 정리했습니다.

### 1. 타겟 브랜치로 체크아웃

먼저 cherry-pick 을 통해 특정 변경사항을 적용할 타겟 브랜치로 체크아웃합니다.

```
git checkout target

```

![](https://velog.velcdn.com/images/joosing/post/26ff6f5d-98ad-4169-82c5-a77e65471c08/image.png)

### 2. 소스 브랜치 커밋 히스토리 보기

타겟 브랜치로 체크아웃 한 상태에서 소스 브랜치 커밋 히스토리를 보면서 가져올 변경사항을 선택하면 편리합니다. 이를 위해 커밋 히스토리 그래프에서 소스브랜치 커밋만 보이도록 필터링합니다. 필요에 따라 특정 사용자, 날짜, 특정 경로의 파일만 필터링하여 가져올 커밋을 쉽게 선택할 수 있습니다.

```
git log source

```

![](https://velog.velcdn.com/images/joosing/post/04e081ff-f3b9-4634-b27c-033ecc08d253/image.png)

### 3. 가져올 커밋 선택하고 Cherry-Pick 하기

이제 커밋 히스토리에서 변경사항을 가져올 소스 브랜치의 커밋들을 선택하고 우클릭 메뉴를 통해 Cherry-Pick 을 수행합니다. 만약 Cherry-Pick 과정에서 충돌이 발생하면 충돌을 해결하고, 최종 변경사항을 커밋해 주어야 합니다.

```
git cherry-pick 1b8f030e

```

![](https://velog.velcdn.com/images/joosing/post/ed6bcf28-e4bd-4f8a-bc34-27a339dea269/image.png)

### 4. Cherry-Pick 완료

이제 필터링 적용했던 사항들을 최종적으로 해제하고 선택한 변경사항이 잘 가져와 졌는지 확인합니다. 아래에서 보시는 것 처럼 소스 브랜치에 있던 변경사항(커밋) B가 타겟 브랜치 헤드 위치에 생성된 것을 확인할 수 있습니다. 여기서 한 가지 기억할 것은 소스 브랜치의 B 커밋과 Cherry-Pick 된 타겟 브랜치의 B 커밋의 해쉬값이 다르다는 것입니다. 두 커밋은 변경의 내용은 같지만 해쉬값이 다른 두 개의 커밋입니다.

```
git log

```

![](https://velog.velcdn.com/images/joosing/post/c7963268-92ad-4630-b64d-d30cadf3d971/image.png)

# Reference

- [https://johngrib.github.io/wiki/git/cherry-pick/](https://johngrib.github.io/wiki/git/cherry-pick/)
- [https://git-scm.com/docs/git-cherry-pick](https://git-scm.com/docs/git-cherry-pick)
