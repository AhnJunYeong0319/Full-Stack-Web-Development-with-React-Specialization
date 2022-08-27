## Exercise (Instructions): Setting up Git

※ 새로운 repository를 만드는 경우
```
git clone https://github.com/AhnJunYeong0319/RepositoryName.git # 이렇게 시작 안해도 되긴 하는데, git clone은 repo에 있는 것을 local에 그대로 가져와주기 때문에 첫 push가 rejected안될 확률이 높음 (시작할때 만드는 README.md같은것도 가져와주기 때문)
<!--------------------------------------------------------------------!>
git init                        # project folder 내에서 .git file 생성
git status                      # staging area에 올라간 파일들 확인 (modified, deleted, created 등으로 구분)
git add . (or) git add A/B/random.html         # 나중에 협업할때나, modules같은 더러운 파일까지 github에 올라갈 수 있으니 하나하나 지정해주는게 좋을 듯 (나중에 reset하기도 쉽고)
git branch -M main              ### 아주 중요한 놈인데, 이걸 꼭 하지 않으면 아무 생각없이 master과 main이 꼬여버린다. 나중에 뭐 어떻게 할 필요 없이, 항상 repo를 만들자마자 on main인 상태로 만들어주자. 이게 잘 먹혔는지는 git branch로 확인 가능
git commit -m "blahblah"        # staging area에 올라왔다고 commit된게 아니다. 늘 git status로 상태를 확인해주자
git remote add origin https://github.com/AhnJunYeong0319/RepositoryName.git        # 원격 저장소와 연결.
git push -u origin main         # push하고 끝.
```

주의할 점으로, git push를 하려고 하는데 rejected되면서 노란색으로 warning이라 해야할지 instruction이라 해야할지 암튼 완전 안되는건 아닌 것 같은데 push는 안되는 상황이 있다.

첫 push가 안되는 상황은 맨 위에서 언급한 것처럼 초기 README.md나 .gitattributes같은 것이 local과 remote가 완전 동일한 상황이 아니기 때문에 git clone으로 시작해주면 해결할 수 있고 (물론 이렇게 안하고 두 번째 방법으로도 처리할 수 있다),

어느 순간 갑자기 push가 rejected되고 노란색 instruction으로 (try git pull …)같은 메세지가 뜬다면,

```git pull origin main          # https://devlog-wjdrbs96.tistory.com/236에 잘 설명되어 있다.```

로 local의 현재 상태 + remote의 상태를 merge해줌으로서 (local + remote → local 이렇게 local을 update해주는 방식이고, local과 remote의 집합관계는 딱히 상관 없을 것 같긴 하나 push가 rejected되는건 99% local이 remote의 부분집합이 되어버린 상태일 것이다 - 멍청하게 레포에서 직접 어떤 파일을 삭제하는 짓을 한게 아닌 추가한거라면.) 준비가 됐다.

이제 걍 다시 push하면 될 것이다 - 아직은 이렇게 해서도 해결이 안된 경우는 못 봄 

※ 그 외 필수 상식 ※

1. .git이란 파일은 숨어있다. 이 파일은 git init 명령어를 통해 생성되는 파일로, local에 있는 directory가 git repo용이라는 뜻이다. 따라서 얘를 보려면 아래와 같이 확인해야한다. 만약 outer (=parent) directory가 git repo용인데, inner (=child)에도 숨어있는 .git이 있는 상태에서 아무 생각없이 github에 올린다면 해결하는데만 6시간이 걸렸던 **nested git**이라는 issue를 다시 만나게 된다………………

![image](https://user-images.githubusercontent.com/63603383/187036943-cf5698ee-2e65-41e9-a9b8-4708d2020ddb.png) <br>
2. branch main과 master를 헷갈리지 말도록. 난 이미 알고 있듯이 master은 과거의 유물이라 main에 넣어야하는데, 문제는 이게 중간에 바뀐거다보니 google에 있는 git command 관련 instruction들이 대부분 master 기준으로 설명하고 있다. 오랜만에 git commit하느라 이걸 다 까먹고 또 멍청하게 git push origin master를 시작했다간 지옥이다. 앞으론 그냥 master란 단어를 머릿속에서 지우고, 첫 push 전 git branch -M main을 통해 main에 위치할 수 있도록 하자. (물론 나중에 내가 깃허브로 협업을 하게 된다면 branch 여러개를 사용하게 되겠지만 아직은 그런 일이 없다)

3. 프로젝트 폴더 이동시 cd A/B/C 커맨드를 이용해서 잘 움직여야 한다. 예시로 react 프로젝트 중이라고 치자. npm start를 통해 local에서 index.html을 열려고 open folder를 통해 가장 가까운 디렉토리에 위치해있을 것이다. 이러면 자연스럽게 terminal에서도 같은 위치에 있을 건데, 이걸 진행하면서 동시에 더 바깥쪽에 있는 git directory (= .git 파일이 있는, git remote 저장소와 연결된, git init을 했던 프로젝트 폴더)에도 위치하고 싶을 때가 있을것이다 - 단순히 실시간으로 깃헙 push할때만 해도.
![image](https://user-images.githubusercontent.com/63603383/187036957-1f24ab5d-1c2c-46cf-b592-ad055b1bd1e9.png) <br>
이럴땐 VSCode에서 terminal 이름 옆에 +를 누르면 별도로 움직이는 다른 cmd가 나와서 편하게 두 개를 동시에 쓰면 된다.

## Exercise (Instructions): Basics of Node.js and NPM
![image](https://user-images.githubusercontent.com/63603383/187037055-c0ce17de-f138-4035-8670-15e553b7745b.png)
![image](https://user-images.githubusercontent.com/63603383/187037076-4a7e7e87-025f-411d-afa9-306f729f8932.png)

## Exercise (Instructions): Getting Started with Bootstrap
![image](https://user-images.githubusercontent.com/63603383/187037120-9033ae1d-d62c-4929-8b5a-1b09729694f5.png)
![image](https://user-images.githubusercontent.com/63603383/187037133-76e65b91-aaf3-4e0c-88ae-7cf21ec71a2e.png)
![image](https://user-images.githubusercontent.com/63603383/187037148-838d0c5e-a276-433f-9f89-3b31398c53bd.png)


