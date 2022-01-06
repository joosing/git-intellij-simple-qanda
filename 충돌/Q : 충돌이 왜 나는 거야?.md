**Q : 충돌이 왜 나는 거야?**  
A : Git은 소스코드 라인을 최소 단위로 변경을 관리해. 그래서 동일한 라인을 두명이 동시에 수정하고 저장소에 커밋하면 Git은 누가 수정한 것을 최종버전으로 할지 결정할 수 없어. 그래서 이건 사람이 정하라고 말해주는 거야! 

**Q : 그럼 A=B 라는 라인에서 한 사람은 A를 다른 사람은 B를 수정해도 충돌이 나겠네?**  
A : 맞아! 이런 경우에는 A와 B의 코드를 합해서 한 라인(A1 = B1)을 만들어 줘야해. 만약 두 사람이 동시에 A를 수정했다면 누구의 것이 맞는지 선택해서 A1 or A2 = B 라인을 만들어 줘야 해!  

**Q : 그래서 충돌은 어떻게 해결해?**  
A : 충돌 시, 머지 메뉴를 선택하면 에디터가 뜨는데 왼쪽(나의 작업 파일), 오른쪽(저장소 파일), 가운데가 충돌을 해결할 최종 버전 에디터 영역이야. 그림과 같은 순서로 해결할 수 있어.

<img src="https://user-images.githubusercontent.com/34666301/148458360-bf7c6d9e-be0f-41f2-83ec-b8a09516401f.png" width="50%" height="50%">

![image](https://user-images.githubusercontent.com/34666301/148458374-66d92cb5-4b01-4d43-9af5-2d6adc93bf0d.png)
![image](https://user-images.githubusercontent.com/34666301/148458751-224da116-7bdc-422c-9557-7cb6f85b4529.png)
![image](https://user-images.githubusercontent.com/34666301/148458434-ebc1a727-2359-4176-8fe3-085756816cee.png)
