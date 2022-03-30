![git+intellij_sized2](https://user-images.githubusercontent.com/34666301/148475812-046ba69c-30be-4df2-994f-7d3071916bac.png)

# git-intellij-simple-QandA
동료들에게 Git 사용과 관련된 문제에 대해 비슷한 질문을 반복해서 받는 것 같습니다. 질문 받은 것들에 대해 Q&A를 간단히 정리해 둡니다. 저장소는 다음과 같은 지향점을 가지고 정리하였습니다.  

> 1. Git 사용중 마주하는 문제를 중심으로 해결 방법을 간단히 기술합니다.  
> 2. Git의 개념과 원리에 대한 설명은 최소화합니다. (정리하고 보니 충돌 카테고리 외에는 개념 설명이 없습니다)       
> 3. IntelliJ 기반 GUI 사용법을 설명합니다. (git command도 시간이 되면 정리하고 싶습니다)   


# 버전활용
[Q : A소스 코드 N라인 누가 마지막에 수정한거지?](https://github.com/Jsing/intellij-git-trouble-qanda/blob/2d054e70d253cf3aa4f5e1d97cefb12d279f9a44/%EB%B2%84%EC%A0%84%ED%99%9C%EC%9A%A9/A%EC%86%8C%EC%8A%A4%20%EC%BD%94%EB%93%9C%20N%EB%9D%BC%EC%9D%B8%20%EB%88%84%EA%B0%80%20%EB%A7%88%EC%A7%80%EB%A7%89%EC%97%90%20%EC%88%98%EC%A0%95%ED%95%9C%EA%B1%B0%EC%A7%80%3F.md) `blame`   
[Q : 특정 커밋에서 발생한 변경사항을 다른 브랜치로 옮기고 싶어](https://github.com/Jsing/intellij-git-trouble-qanda/blob/13a89432c02bbcd6fe797d67dce1c44ef121c7ed/%EB%B2%84%EC%A0%84%ED%99%9C%EC%9A%A9/Q%20:%20%ED%8A%B9%EC%A0%95%20%EC%BB%A4%EB%B0%8B%EC%97%90%EC%84%9C%20%EB%B0%9C%EC%83%9D%ED%95%9C%20%EB%B3%80%EA%B2%BD%EC%82%AC%ED%95%AD%EC%9D%84%20%EB%8B%A4%EB%A5%B8%20%EB%B8%8C%EB%9E%9C%EC%B9%98%EB%A1%9C%20%EC%98%AE%EA%B8%B0%EA%B3%A0%20%EC%8B%B6%EC%96%B4.md) `patch`  

# 충돌
[Q : 충돌이 왜 나는 거야?](https://github.com/Jsing/intellij-git-trouble-qanda/blob/1bae99cc5506079265b95accf435155d93811864/%EC%B6%A9%EB%8F%8C/Q%20:%20%EC%B6%A9%EB%8F%8C%EC%9D%B4%20%EC%99%9C%20%EB%82%98%EB%8A%94%20%EA%B1%B0%EC%95%BC%3F.md) `conflict`  
[Q : 그래서 충돌은 어떻게 해결해?](https://github.com/Jsing/intellij-git-trouble-qanda/blob/1bae99cc5506079265b95accf435155d93811864/%EC%B6%A9%EB%8F%8C/Q%20:%20%EC%B6%A9%EB%8F%8C%EC%9D%B4%20%EC%99%9C%20%EB%82%98%EB%8A%94%20%EA%B1%B0%EC%95%BC%3F.md) `resolve` 

# 돌아가기
[Q : 지금 뭔가 잘못 코딩하고 있는 것 같아. 직전 커밋 상태로 깨끗하게 돌리고 싶어. ](https://github.com/Jsing/intellij-git-trouble-qanda/blob/c6b5553285e6b0e63023800674e53c73651626a6/%EB%8F%8C%EC%95%84%EA%B0%80%EA%B8%B0/Q%20:%20%EC%A7%80%EA%B8%88%20%EB%AD%94%EA%B0%80%20%EC%9E%98%EB%AA%BB%20%EC%BD%94%EB%94%A9%ED%95%98%EA%B3%A0%20%EC%9E%88%EB%8A%94%20%EA%B2%83%20%EA%B0%99%EC%95%84.%20%EC%A7%81%EC%A0%84%20%EC%BB%A4%EB%B0%8B%20%EC%83%81%ED%83%9C%EB%A1%9C%20%EA%B9%A8%EB%81%97%ED%95%98%EA%B2%8C%20%EB%8F%8C%EB%A6%AC%EA%B3%A0%20%EC%8B%B6%EC%96%B4.md) `roll-back`  
[Q : 특정 커밋의 변경사항을 되돌려야 하는데, 다음에 다시 사용하게 이력은 남기고 싶어 ](https://github.com/Jsing/intellij-git-trouble-qanda/blob/63f9801b5658502c8167bb3dc4bd3ed190cf2464/%EB%8F%8C%EC%95%84%EA%B0%80%EA%B8%B0/Q%20:%20%ED%8A%B9%EC%A0%95%20%EC%BB%A4%EB%B0%8B%EC%9D%98%20%EB%B3%80%EA%B2%BD%EC%82%AC%ED%95%AD%EC%9D%84%20%EB%90%98%EB%8F%8C%EB%A0%A4%EC%95%BC%20%ED%95%98%EB%8A%94%EB%8D%B0,%20%EB%8B%A4%EC%9D%8C%EC%97%90%20%EB%8B%A4%EC%8B%9C%20%EC%82%AC%EC%9A%A9%ED%95%98%EA%B2%8C%20%EC%9D%B4%EB%A0%A5%EC%9D%80%20%EB%82%A8%EA%B8%B0%EA%B3%A0%20%EC%8B%B6%EC%96%B4%20.md) `revert`  
[Q : 뭔가 완전히 잘못되었어! 브랜치를 특정 커밋 지점으로 완전히 돌아가고 싶어! 커밋된 변경도 다 삭제하고 싶어!](https://github.com/Jsing/intellij-git-trouble-qanda/blob/92823d5624825fbff614f14e8cf3d485a6c0e282/%EB%8F%8C%EC%95%84%EA%B0%80%EA%B8%B0/Q%20:%20%EB%AD%94%EA%B0%80%20%EC%99%84%EC%A0%84%ED%9E%88%20%EC%9E%98%EB%AA%BB%EB%90%98%EC%97%88%EC%96%B4!%20%EB%B8%8C%EB%9E%9C%EC%B9%98%EB%A5%BC%20%ED%8A%B9%EC%A0%95%20%EC%BB%A4%EB%B0%8B%20%EC%A7%80%EC%A0%90%EC%9C%BC%EB%A1%9C%20%EC%99%84%EC%A0%84%ED%9E%88%20%EB%8F%8C%EC%95%84%EA%B0%80%EA%B3%A0%20%EC%8B%B6%EC%96%B4!%20%EC%BB%A4%EB%B0%8B%EB%90%9C%20%EB%B3%80%EA%B2%BD%EB%8F%84%20%EB%8B%A4%20%EC%82%AD%EC%A0%9C%ED%95%98%EA%B3%A0%20%EC%8B%B6%EC%96%B4!.md)  `reset --hard`  
[Q : 브랜치를 특정 커밋 지점으로 돌리면서, 해당 커밋 이후에 발생한 변경 사항들은 워킹 디렉토리에 유지하고 싶어. ](https://github.com/Jsing/intellij-git-trouble-qanda/blob/c2ffabfcad778247c2780188efecf502a9933257/%EB%8F%8C%EC%95%84%EA%B0%80%EA%B8%B0/Q%20:%20%EB%B8%8C%EB%9E%9C%EC%B9%98%EB%A5%BC%20%ED%8A%B9%EC%A0%95%20%EC%BB%A4%EB%B0%8B%20%EC%A7%80%EC%A0%90%EC%9C%BC%EB%A1%9C%20%EB%8F%8C%EB%A6%AC%EB%A9%B4%EC%84%9C,%20%ED%95%B4%EB%8B%B9%20%EC%BB%A4%EB%B0%8B%20%EC%9D%B4%ED%9B%84%EC%97%90%20%EB%B0%9C%EC%83%9D%ED%95%9C%20%EB%B3%80%EA%B2%BD%20%EC%82%AC%ED%95%AD%EB%93%A4%EC%9D%80%20%EC%9B%8C%ED%82%B9%20%EB%94%94%EB%A0%89%ED%86%A0%EB%A6%AC%EC%97%90%20%EC%9C%A0%EC%A7%80%ED%95%98%EA%B3%A0%20%EC%8B%B6%EC%96%B4.md)  `reset --soft`   
[Q : Reset 후 원격 저장소에 Push 하면 Push Reject 되네. Merge나 Rebase 하면 자꾸 Reset한 걸 다시 가져와... 내걸로 원격 저장소를 덮어쓰고 싶은데](https://github.com/Jsing/intellij-git-trouble-qanda/blob/47c52abae81961bcc09ce79087a732af0c023c3f/%EB%8F%8C%EC%95%84%EA%B0%80%EA%B8%B0/Q%20:%20Reset%20%ED%9B%84%20%EC%9B%90%EA%B2%A9%20%EC%A0%80%EC%9E%A5%EC%86%8C%EC%97%90%20Push%20%ED%95%98%EB%A9%B4%20Push%20Reject%20%EB%90%98%EB%84%A4.%20Merge%EB%82%98%20Rebase%20%ED%95%98%EB%A9%B4%20%EC%9E%90%EA%BE%B8%20Reset%ED%95%9C%20%EA%B1%B8%20%EB%8B%A4%EC%8B%9C%20%EA%B0%80%EC%A0%B8%EC%99%80...%20%EB%82%B4%EA%B1%B8%EB%A1%9C%20%EC%9B%90%EA%B2%A9%20%EC%A0%80%EC%9E%A5%EC%86%8C%EB%A5%BC%20%EB%8D%AE%EC%96%B4%EC%93%B0%EA%B3%A0%20%EC%8B%B6%EC%9D%80%EB%8D%B0.md)  `push --force`    
[Q : 마스터 브랜치에 실수로 Merge 를 해버렸어. 깔금하게 Merge 이전으로 돌리고 싶은데?](https://github.com/Jsing/git-intellij-simple-qanda/blob/be2cf44f1fe6916b5df874ccb503511a93182ef3/%EB%8F%8C%EC%95%84%EA%B0%80%EA%B8%B0/Q%20:%20%EB%A7%88%EC%8A%A4%ED%84%B0%20%EB%B8%8C%EB%9E%9C%EC%B9%98%EC%97%90%20%EC%8B%A4%EC%88%98%EB%A1%9C%20Merge%20%EB%A5%BC%20%ED%95%B4%EB%B2%84%EB%A0%B8%EC%96%B4.%20%EA%B9%94%EA%B8%88%ED%95%98%EA%B2%8C%20Merge%20%EC%9D%B4%EC%A0%84%EC%9C%BC%EB%A1%9C%20%EB%8F%8C%EB%A6%AC%EA%B3%A0%20%EC%8B%B6%EC%9D%80%EB%8D%B0%3F.md)  
[Q : Amend 해서 하나로 합치기 전으로 다시 돌아가고 싶은데?](https://github.com/Jsing/git-intellij-simple-qanda/blob/39edd8f6045b5afc71e9cb0341aee7436a786f9d/%EB%8F%8C%EC%95%84%EA%B0%80%EA%B8%B0/Q%20:%20Amend%20%ED%95%B4%EC%84%9C%20%ED%95%98%EB%82%98%EB%A1%9C%20%ED%95%A9%EC%B9%98%EA%B8%B0%20%EC%A0%84%EC%9C%BC%EB%A1%9C%20%EB%8B%A4%EC%8B%9C%20%EB%8F%8C%EC%95%84%EA%B0%80%EA%B3%A0%20%EC%8B%B6%EC%9D%80%EB%8D%B0.md) `reflog`  

# 버전관리
[Q : 지금 개발중이라 빌드가 안되는 상태인데, 잠시 다른 브랜치로 이동해서 작업하고 싶은데, 이걸 커밋해 두기는 애매하네 어떻하지? ](https://github.com/Jsing/intellij-git-trouble-qanda/blob/c9bdc972a185e98da479730ee5cf90880ff6d28a/%EB%B2%84%EC%A0%84%EA%B4%80%EB%A6%AC/Q%20:%20%EC%A7%80%EA%B8%88%20%EA%B0%9C%EB%B0%9C%EC%A4%91%EC%9D%B4%EB%9D%BC%20%EB%B9%8C%EB%93%9C%EA%B0%80%20%EC%95%88%EB%90%98%EB%8A%94%20%EC%83%81%ED%83%9C%EC%9D%B8%EB%8D%B0,%20%EC%9E%A0%EC%8B%9C%20%EB%8B%A4%EB%A5%B8%20%EB%B8%8C%EB%9E%9C%EC%B9%98%EB%A1%9C%20%EC%9D%B4%EB%8F%99%ED%95%B4%EC%84%9C%20%EC%9E%91%EC%97%85%ED%95%98%EA%B3%A0%20%EC%8B%B6%EC%9D%80%EB%8D%B0,%20%EC%9D%B4%EA%B1%B8%20%EC%BB%A4%EB%B0%8B%ED%95%B4%20%EB%91%90%EA%B8%B0%EB%8A%94%20%EC%95%A0%EB%A7%A4%ED%95%98%EB%84%A4%20%EC%96%B4%EB%96%BB%ED%95%98%EC%A7%80%3F.md)  `stash`  
[Q : 브랜치 옆에 표시되는 이 화살표는 뭐야? ](https://github.com/Jsing/intellij-git-trouble-qanda/blob/2d3a1dd5b5a31948a918e1b07d14ab188d1d122b/%EB%B2%84%EC%A0%84%EA%B4%80%EB%A6%AC/Q%20:%20%EB%B8%8C%EB%9E%9C%EC%B9%98%20%EC%98%86%EC%97%90%20%ED%91%9C%EC%8B%9C%EB%90%98%EB%8A%94%20%EC%9D%B4%20%ED%99%94%EC%82%B4%ED%91%9C%EB%8A%94%20%EB%AD%90%EC%95%BC%3F.md) `out-of-date`  

# 커밋관리
[Q : 방금 A 커밋을 생성했는데, 코드를 조금 수정해서 커밋 A 에 포함시키고 싶어](https://github.com/Jsing/git-intellij-simple-qanda/blob/2f6bfed2f85f670d61971f2cf18b8f5828ed1eb6/%EC%BB%A4%EB%B0%8B%EA%B4%80%EB%A6%AC/Q%20:%20%EB%B0%A9%EA%B8%88%20A%20%EC%BB%A4%EB%B0%8B%EC%9D%84%20%EC%83%9D%EC%84%B1%ED%96%88%EB%8A%94%EB%8D%B0,%20%EC%BD%94%EB%93%9C%EB%A5%BC%20%EC%A1%B0%EA%B8%88%20%EC%88%98%EC%A0%95%ED%95%B4%EC%84%9C%20%EC%BB%A4%EB%B0%8B%20A%20%EC%97%90%20%ED%8F%AC%ED%95%A8%EC%8B%9C%ED%82%A4%EA%B3%A0%20%EC%8B%B6%EC%96%B4.md) `amend`  
