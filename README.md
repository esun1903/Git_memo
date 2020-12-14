# Git ( Version Control System )

Git - Version Control System 중 한 시스템이다. 

report.xls  → report_final_real_final.xls 이렇게 해야하는 것 

Version Management not by changing the file name 

1. Backup  2. Recovery 3. Collaboration

Version Control Systems → CVS , SVN , GIT 가 있다. 

Git is incredibly complex → 믿어지지않을만큼 복잡하다. 

버전 컨트롤 시스템 → dropbox, google Drive 같은 사용하기 쉬운 것들을 바탕으로 하기 

자신이 어느 상황이냐에 따라 git, google Drive를 사용하기 

✅ **git** : Start a working area : 작업장에서 작업을 시작하겠다. 

      - 1. Clone , 2. init 

✅ **init** : 현재 디텍토리에 내가 작업을 진행하겠다라는 것을 깃에게 알려주는 것 

```jsx
 git init 
```

ls -al : 현재 디렉토리에 어떤 것이 있는지 보여주려는 것 

cat f1.txt : 하면 txt파일의 내용이 보여진다. 

![Untitled](https://user-images.githubusercontent.com/38427646/102079499-28ef2880-3e50-11eb-9ece-5c3c356fcfb7.png)

- 지금 생성한 f1.txt 파일은 버전관리가 되고 있는 디렉토리인 gitfth 안에는 존재하지만

 우리가 이 파일을 버전관리를 시작해라고 얘기하기 전까지는 깃은 얘를 무시합니다. 

 ✅ **add :** 깃에게 이 f1.txt파일을 버전관리를 시작하라고 말을 해야함! 이 때, 사용되는 명령어가 add 이다. , 파일을 수정해서 버전을 만들기 전에도 마찬가지입니다.

```jsx
git add f1.txt 
```

![Untitled 1](https://user-images.githubusercontent.com/38427646/102079411-03fab580-3e50-11eb-8b06-6fe9c8321b24.png)

- git add 를 하면 아까와는 다르게 status시 git이 new file이라고 인식한다.

```jsx
git config --global user.name 닉네임
git config --global user.email 이메일
```

- 다른 사람이 봤을때 누가 작업했는지 알 수 있는 것으로 나의 닉네임과 이메일을 넣으면 된다.  ( 이건 딱 한번만 하면된다. )

 ✅ **commit** : 현재 버전의 메시지를 적는 것 , 이 변화가 어떤변화로 되었는지, 파일이 왜 변경되었는지 ! 

 

![Untitled 2](https://user-images.githubusercontent.com/38427646/102079564-4a501480-3e50-11eb-8dda-cc1be8148997.png)

- 이렇게 하면 잘 된 것
- 보통 git commit -m "메시지" 이렇게 한다.
- -a  : add 와 같이 하는 명령어
- -am : add 명령어와 m를 할 수 있는 명령어
- git commit —help 로 다양한 것을 알 수 있다.

log : 로그를 확인하면 commit 등 내가 지금까지 했던 commit 들을 보여집니다. 

✅ **diff** : 두 커밋 사이의 다른 점을 알고 싶을때 사용하는 것 

![Untitled 3](https://user-images.githubusercontent.com/38427646/102079589-55a34000-3e50-11eb-8a09-ca2b113c49bd.png)

![Untitled 4](https://user-images.githubusercontent.com/38427646/102079607-5c31b780-3e50-11eb-9411-3e7b6be435b8.png)

- git diff를 통해 내가 현재 어떤작업을 했는지 전 → 후를 알 수 있습니다.
- commit를 하기 전 내가 한 작업이 잘됐는지 안됐는지를 확인할 수 있는 마지막 기회! 를 제공합니다.

![Untitled 5](https://user-images.githubusercontent.com/38427646/102079625-6358c580-3e50-11eb-83ac-de1202be5d43.png)

- reset : commit 를 지우고 다시하는 명령어 ( 나중에 soft를 배운다. hard는 조금 위험하다는 것)

revert : commit 를 지우고 다시하는 명령어

![Untitled 6](https://user-images.githubusercontent.com/38427646/102079648-6bb10080-3e50-11eb-9b2b-f75863ed4491.png)

- 생활코딩에서 나온 사람들이 자주 검색하는 git 명령어들 (중요도 순이라고 할 수 있겠다. )

✅  **branch** : 나뭇가지

report.xsl → report1.xsl → report2.xsl 순으로 수정되는 파일이 있다고 생각해보자. 

이 파일을 일부 수정하여 client에게 준다고 생각하자. 

report2.xsl → report2_client.xsl → report_client2.xsl  ———> 

                                                                                                     reposrt5.xsl       →  report6.xsl 
    
                  → report3.xsl → reporst4.xsl                   ——— > 

![Untitled 7](https://user-images.githubusercontent.com/38427646/102079667-753a6880-3e50-11eb-97e5-e47c9b5fbc39.png)

- git branch : 브랜치를 만드는 명령어

![Untitled 8](https://user-images.githubusercontent.com/38427646/102079697-7f5c6700-3e50-11eb-93e8-fc28465f4e7c.png)

- git checkout exp 는 현재 브랜치인 master를 체크아웃하고 exp로 하겠다는 것을 의미합니다.

![Untitled 9](https://user-images.githubusercontent.com/38427646/102079716-86837500-3e50-11eb-8b7f-866cd080e538.png)

- git log —braches —decorate는 모든 branch git log별로 최신 commit 이 보여진다.

![Untitled 10](https://user-images.githubusercontent.com/38427646/102079739-8daa8300-3e50-11eb-94ff-f8570b626805.png)

- — graph를 통해  5와 3,4는 2이라는 공통에서 나온 것을 알 수 있습니다.

![Untitled 11](https://user-images.githubusercontent.com/38427646/102079766-9b600880-3e50-11eb-8512-d05fc96f1ea6.png)

- — oneline 를 하면 좀 더 간결하게 볼 수 있습니다.

![Untitled 12](https://user-images.githubusercontent.com/38427646/102079784-a1ee8000-3e50-11eb-9ced-2db8e0e852d4.png)

- log 와  exp를 비교하는 것을 의미한다.
- log에는 없고 exp에는 있는 것을 보여줌 ! (만약 git log exp..master를 하면  exp에는 없고 master에는 있는 것을 알려준다. )

✅ **merge** : 브랜치 병합 

![Untitled 13](https://user-images.githubusercontent.com/38427646/102079822-b6327d00-3e50-11eb-9ba4-54fe0a14f8d1.png)

![Untitled 14](https://user-images.githubusercontent.com/38427646/102079849-c0547b80-3e50-11eb-9a2f-c95e69429c91.png)


- 생활코딩 (유튜브 생활코딩) 
