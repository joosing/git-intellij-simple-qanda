**Q : Amend 해서 하나로 합치기 전으로 다시 돌아가고 싶은데?**   

A : Intellij 에서 Teminal 열고 (Alt + F12) 
  1) git reflog (head reference history)
  2) amend 이전 커밋 해쉬값을 확인
  3) git reset --soft 해쉬값 (or --hard)

![image](https://user-images.githubusercontent.com/34666301/159056623-42ad47be-411a-406f-8772-db423d9b6696.png)
