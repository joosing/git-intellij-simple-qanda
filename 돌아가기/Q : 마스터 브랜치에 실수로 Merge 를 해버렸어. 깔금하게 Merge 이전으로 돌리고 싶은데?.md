**Q : 마스터 브랜치에 실수로 Merge 를 해버렸어. 깔금하게 Merge 이전으로 돌리고 싶은데?**   

A : 일단 reset 기능을 사용하면 되는데, 어느 커밋으로 reset 해야 하는지가 문제야. <1. 실수로 merge 된 master 브랜치> 이미지를 보면 초록색 브랜치(Master)와 보라색 브랜치가 머지된 결과야. 
우리가 원하는 건 Master 1 커밋을 한 상태로 돌아가면서 보라색 브런치 내용은 다 제거하는 거야. 그림 <2. 복구된 master 브랜치> 처럼 말이야. 방법은 간단해
1. master 브랜치로 체크아웃
2. 만일에 사태에 대비해 master 브랜치의 백업 브랜치 생성
3. Git 로그 그래프에서 'Master 1' 커밋 우클릭
4. Reset Current Branch to Here' 메뉴 선택
5. Hard 옵션 선택 (또는 Soft, 아래 Hard/Soft Reset Reference 참조)
6. Force Push 

※ Reference  
- [Hard Reset](https://github.com/Jsing/git-intellij-simple-qanda/blob/92823d5624825fbff614f14e8cf3d485a6c0e282/%EB%8F%8C%EC%95%84%EA%B0%80%EA%B8%B0/Q%20:%20%EB%AD%94%EA%B0%80%20%EC%99%84%EC%A0%84%ED%9E%88%20%EC%9E%98%EB%AA%BB%EB%90%98%EC%97%88%EC%96%B4!%20%EB%B8%8C%EB%9E%9C%EC%B9%98%EB%A5%BC%20%ED%8A%B9%EC%A0%95%20%EC%BB%A4%EB%B0%8B%20%EC%A7%80%EC%A0%90%EC%9C%BC%EB%A1%9C%20%EC%99%84%EC%A0%84%ED%9E%88%20%EB%8F%8C%EC%95%84%EA%B0%80%EA%B3%A0%20%EC%8B%B6%EC%96%B4!%20%EC%BB%A4%EB%B0%8B%EB%90%9C%20%EB%B3%80%EA%B2%BD%EB%8F%84%20%EB%8B%A4%20%EC%82%AD%EC%A0%9C%ED%95%98%EA%B3%A0%20%EC%8B%B6%EC%96%B4!.md)  
- [Soft Reset](https://github.com/Jsing/git-intellij-simple-qanda/blob/c2ffabfcad778247c2780188efecf502a9933257/%EB%8F%8C%EC%95%84%EA%B0%80%EA%B8%B0/Q%20:%20%EB%B8%8C%EB%9E%9C%EC%B9%98%EB%A5%BC%20%ED%8A%B9%EC%A0%95%20%EC%BB%A4%EB%B0%8B%20%EC%A7%80%EC%A0%90%EC%9C%BC%EB%A1%9C%20%EB%8F%8C%EB%A6%AC%EB%A9%B4%EC%84%9C,%20%ED%95%B4%EB%8B%B9%20%EC%BB%A4%EB%B0%8B%20%EC%9D%B4%ED%9B%84%EC%97%90%20%EB%B0%9C%EC%83%9D%ED%95%9C%20%EB%B3%80%EA%B2%BD%20%EC%82%AC%ED%95%AD%EB%93%A4%EC%9D%80%20%EC%9B%8C%ED%82%B9%20%EB%94%94%EB%A0%89%ED%86%A0%EB%A6%AC%EC%97%90%20%EC%9C%A0%EC%A7%80%ED%95%98%EA%B3%A0%20%EC%8B%B6%EC%96%B4.md)  
- [Force Push](https://github.com/Jsing/git-intellij-simple-qanda/blob/47c52abae81961bcc09ce79087a732af0c023c3f/%EB%8F%8C%EC%95%84%EA%B0%80%EA%B8%B0/Q%20:%20Reset%20%ED%9B%84%20%EC%9B%90%EA%B2%A9%20%EC%A0%80%EC%9E%A5%EC%86%8C%EC%97%90%20Push%20%ED%95%98%EB%A9%B4%20Push%20Reject%20%EB%90%98%EB%84%A4.%20Merge%EB%82%98%20Rebase%20%ED%95%98%EB%A9%B4%20%EC%9E%90%EA%BE%B8%20Reset%ED%95%9C%20%EA%B1%B8%20%EB%8B%A4%EC%8B%9C%20%EA%B0%80%EC%A0%B8%EC%99%80...%20%EB%82%B4%EA%B1%B8%EB%A1%9C%20%EC%9B%90%EA%B2%A9%20%EC%A0%80%EC%9E%A5%EC%86%8C%EB%A5%BC%20%EB%8D%AE%EC%96%B4%EC%93%B0%EA%B3%A0%20%EC%8B%B6%EC%9D%80%EB%8D%B0.md)  

![image](https://user-images.githubusercontent.com/34666301/160736657-a137fe67-1773-4a51-ba90-8a212b9d016d.png)  
<1. 실수로 merge 된 master 브랜치>

![image](https://user-images.githubusercontent.com/34666301/160738630-72b8883b-5d83-4526-aa59-956512e36fd8.png)  
<2. 복구된 master 브랜치>
