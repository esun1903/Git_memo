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
##### git add의 다양한 옵션 

 - git add. 현재 디렉토리 추가
 - git add  -u 수정된 부분 추가
 - git add  -A 폴더 있는 모든 파일 추가
 - git add  -i 파일을 추가할댸 대화식으로 추가하기
 - git add  * 모든 파일을 staged 상태로 만듬 -> .gitigonore 무시하고 올라갈수도 있음
 - git add  -p 수정된거 확인 후 추가하기

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


![Untitled 15](https://user-images.githubusercontent.com/38427646/102196069-bd19c800-3f02-11eb-81ff-1ee11c8fb156.png)

- Fast-forward - 빠른감기 시 merge를 해도 master가 가르키는 커밋이 누구인지를 바꾸는 것

✅ **stash** : 감추다 , 숨겨두다 → 브랜치를 가지고 작업을 하다보면 작업하던 도중 다른브랜치로 checkout을 할 때가 있다. 그런경우 작업이 끝나기전에 commit하기도 애매하고 할 상황에 작업하던 것을 잠깐 숨겨둘 수 있다. 



- git stash를 통해 stash를 진행할 수 있다. → 해당 f1.txt는 수정하기 전(a)

  으로 되어있다. 

  ![Untitled 16](https://user-images.githubusercontent.com/38427646/102196098-c60a9980-3f02-11eb-9b8d-349311c67ab2.png)

![Untitled 17](https://user-images.githubusercontent.com/38427646/102196103-c7d45d00-3f02-11eb-8031-4e812d84775b.png)

- git stash apply를 하면 수정했던 내용 (a b) 가 있다.
- stash는 명시적으로 삭제하지 않는 한 살아있다. (git stash list 로 알 수 있음)

✅ **Head와 branch :** git을 처음 만들면 Head라는 파일이 반드시 생성된다. heads는 master를 가르키는 것을 볼 수 있습니다. 

1. head는 refs/heads/master를 가르키고 master파일에 적혀있는 커밋 objectid값을 통해 가장 최신 커밋이 뭔지 알아낼 수 있다! 그 전파일들은 parent를 통해 ! 알 수 있다. 

✅ **branch 충돌해결**

- 같은 파일에도 수정한 부분이 다르다면 merge를 했을때엔 충돌나지 않는다!
- 하지만, 같은 파일에서 수정한 부분이 같다면 merge를 했을때 충돌난다.
- 

![Untitled 18](https://user-images.githubusercontent.com/38427646/102196108-c9058a00-3f02-11eb-889b-487054258d2b.png)

- 충돌났을 때에 해결하는 법  =======이게 구분자다 ! 🙂
- 음 , 충돌났을 때에 → 해결하는 법은 연습을 많이 해봐야할것같다.

✅**reset**  - commit 을 취소하고 돌아가고 싶을 때  , 브랜치의 최신커밋을 바꾸는 것 

![Untitled 19](https://user-images.githubusercontent.com/38427646/102196112-cacf4d80-3f02-11eb-946d-e0510c883682.png)

- HEAD가 이제 96~ 을 가르킨다. (최신 커밋)

![Untitled 20](https://user-images.githubusercontent.com/38427646/102196118-cc991100-3f02-11eb-865e-9db6724adcbc.png)

- reset 한 것을 취소하고 싶다면 git reset —hard ORIG_HEAD를 하면 됨 gitstory를 보면 orig_head에는 git reset 하기 전 최신 커밋이 남아있습니다.

![Untitled 21](https://user-images.githubusercontent.com/38427646/102196124-d02c9800-3f02-11eb-96f1-cd4caecb31fd.png)

- git reflog 를 통해 지금까지 했던 각각의 커밋들이 기록되어있습니다.

      여기에 HEAD@{0} ~ {6}까지 있는데 이걸 이용해서도 돌아갈 수 있습니다. 

✅ **merge & conflict** 

![Untitled 22](https://user-images.githubusercontent.com/38427646/102196133-d28ef200-3f02-11eb-8b40-1544c86dcd94.png)

![Untitled 23](https://user-images.githubusercontent.com/38427646/102196415-3a453d00-3f03-11eb-8046-91a79b765cc5.png)

- 공통적인 내용이 있다 . (주로 base라고 부른다. )

![Untitled 24](https://user-images.githubusercontent.com/38427646/102196417-3addd380-3f03-11eb-81e4-d9910ad65d08.png)

- 생활코딩에서는 kdiff3이라는 툴을 사용하여 이렇게 직접  수정하고 종료하면 자동으로 merge가 된다.

✅  **3way merge**

![Untitled 25](https://user-images.githubusercontent.com/38427646/102196388-331e2f00-3f03-11eb-9892-e761d7944745.png)

✅  **원격저장소 :** 원격저장소라 함은 지역저장소와는 반대의 의미! 일반적으로 원격저장소라함음 인터넷에 연결되어 다른사람들과 공유할 수 있다는 것 

git init —bare

git push 명령어 ! 

✅  **git clone https :** 로컬저장소에 원격저장소에 있었던 것이 복제됨 . 

✅ **fork :** 포크를 통해 자신의 프로젝트가 되는 것을 알려준다. ( 나의 프로젝트가 되면서 마음대로 소스코드를 수정할 수 있게됨) 

✅ **Git repository** 

![Untitled 26](https://user-images.githubusercontent.com/38427646/102196394-344f5c00-3f03-11eb-995a-4b94cbe74b65.png)

- 원격저장소를 연결시킨다. 이 주소가 기억하기 어려우니 origin이라는 별명을 만들거다. 라는 의미

![Untitled 27](https://user-images.githubusercontent.com/38427646/102196395-34e7f280-3f03-11eb-8e51-52c3ab62b32f.png)


- git remote 로 확인 ! -v로 어떻게 되있는지 확인 ! 🙂

✅ **git pull** 

![Untitled 30](https://user-images.githubusercontent.com/38427646/102196401-35808900-3f03-11eb-9a32-a833ffc3bb86.png)

- git_home 이 있고 git_office가 있다고 생각하자.

      ( office는 회사에서 쓰는 것 , home은 개인 pc → 같은 repository 를 clone한 상태 ) 

- 만약  home에서 push를 하면 그 다음날 office에서는 전 날 작업하던 것이 있으므로 pull을 해서 땡겨쓰는 것을 의미 → 백업이 되는것 ! 😇 💫

✅ **Git Flow** 

![Untitled 31](https://user-images.githubusercontent.com/38427646/102196403-36191f80-3f03-11eb-90f6-21e9ac75da40.png)

1. gitFlow에서는 master에서 개발이 진행되지 않고 develop이라는 branch에서 진행됨 

 2. 개발을 쭉하다가 특정기능을 개발해야할 때에는 feature라는 브랜치를 만들어서 개발을 진행한다. 

3. 그 다음 개발을 완료하면 feature에 있던 브랜치를 develop으로 병합합니다. 버그는 develop으로 해나간다. 

4. 작업을 마무리하고 사용자들에게 배포할 시점이 온다. (웹과 같은 온라인서비스라면 서버에 반영하는 시점 ) → 이 때에 release라는 브랜치를 만든다.  

5. release에서 할 때 버그나 문서작업은 release에서 작업을 하다가 조금씩 조금씩 develop 브랜치에 틈틈히 merge를 함 

6. 충분히 작업이 잘되고 테스트도 잘된다면 실제로 서버에 release를 하는 그 순간에 master로 병합한다. 깃에  tag라는 기능을 통해 1.0 버전의 release는 master 브랜치의 잇커밋,,?이다? ( ,,, 잇커밋은 뭘까,,! → 질문하기 ) 또한 이것은 계속 진행되어야되기 때문에 develop에도 merge를 합니다.

번외 : hoxfixes라는 것은 서비스를 운영하다보면 긴급하게 버그가 날 수 있다. 짧은시간에  처리해야되기 때문에 얼른 처리를 하고 master 브랜치로 merge를 하고 tag로 기록한다. hoxfixes 또한 develop에도 merge를 한다. 

![Untitled 32](https://user-images.githubusercontent.com/38427646/102196405-36b1b600-3f03-11eb-82d3-c9da1e951186.png)

[https://www.youtube.com/watch?v=_kxjzlH34xc&list=PLuHgQVnccGMA8iwZwrGyNXCGy2LAAsTXk&index=49](https://www.youtube.com/watch?v=_kxjzlH34xc&list=PLuHgQVnccGMA8iwZwrGyNXCGy2LAAsTXk&index=49)

실습한 것 



![Untitled 33](https://user-images.githubusercontent.com/38427646/102196407-36b1b600-3f03-11eb-86ac-34d462e424b2.png)

- 이런식으로 했다 . 🙂

아직 많이 부족하지만 git을 점점 활용하면 할수록 좀더 효율적인 개발을 할 수 있다는것 !  

자주자주 공부하는 것이 좋을것같다. 

생활코딩 최고 ㅠㅠㅠ 😇 너무 좋은강의인 것 같다.

- 생활코딩 (유튜브 생활코딩) 

- git 연결할 때 유용한 블로그! :) 
[https://mosei.tistory.com/entry/기존-프로젝트를-git-repository에-연결-하기](https://mosei.tistory.com/entry/%EA%B8%B0%EC%A1%B4-%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%EB%A5%BC-git-repository%EC%97%90-%EC%97%B0%EA%B2%B0-%ED%95%98%EA%B8%B0)

- git 브랜치에 대한 유용한 블로그 :) 
https://mosei.tistory.com/entry/%EA%B8%B0%EC%A1%B4-%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%EB%A5%BC-git-repository%EC%97%90-%EC%97%B0%EA%B2%B0-%ED%95%98%EA%B8%B0ㅠㄱ
