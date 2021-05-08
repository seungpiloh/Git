# Git Practice
## Github repository URL
 https://github.com/seungpiloh/Git.git
## config
- 처음 git을 설치하면 아무 설정도 되어있지 않을 것이다.
- 그러나 git은 커밋 할 때마다 사용자 이름과 이메일 주소를 사용한다. 따라서 git의 최초설정을 해주는 명령어가 필요하다.
- 이를 위해 git 명령어 ‘git config --global' 을 사용하였다.
- 따라서 config 명령어는 git의 최초설정을 위한 명령어이며, 특히 --global 옵션을 사용하여 사용자의 이름과 이메일 주소등을 설정하기 위해 사용하는 것이라 할 수 있다. 그리고 config 명령어의 자주 사용할 것 같은 또 다른 옵션으로는 ‘git config --list' 가 있다. 이 옵션은 설정된 목록을 확인할 수 있도록 해준다.

![1](https://user-images.githubusercontent.com/80791532/117534183-4d2fe980-b02b-11eb-95d7-d4925b9ee07e.PNG)

![2](https://user-images.githubusercontent.com/80791532/117534195-58831500-b02b-11eb-8b44-638317c9ca6b.PNG)

![3](https://user-images.githubusercontent.com/80791532/117534223-72245c80-b02b-11eb-8787-e03f5eeb863d.PNG)

## init
- git을 사용하기 위한 최초 설정은 하였지만 아직 아무것도 할 수 없는 상태이다.
- 따라서 git이 버전관리를 해주는 상태로 만들어주는 명령어가 필요하다.
- 이를 위해 git 명령어 'init'을 사용하였다.
- 따라서, init 명령어는 현재 자신이 위치하고 있는 디렉터리를 기준으로 git 저장소를 생성하여 자신이 위치하고 있는 폴더가 git의 관리 하에 들어가게 하기 위해 사용되는 것으로 정리할 수 있다. 그리고 init 명령어의 자주 사용할 것 같은 또 다른 옵션으로는 ‘git init --bare' 가 있다. 이 옵션은 로컬 저장소가 아닌 원격저장소를 생성해준다.

![3](https://user-images.githubusercontent.com/80791532/117534266-954f0c00-b02b-11eb-9919-9ad04b5ff9ba.PNG)

## status
- 현재 문서가 위치하고 있는 디렉터리는 git의 관리 하에 있다.
-이 때 디렉터리 안의 파일이 수정되었는지 파일의 상태를 확인하고 싶다.
- 이를 위해 git 명령어 ‘status’를 사용하였다.
- 따라서, 이 'status' 명령어는 파일을 수정하였는지(git이 파일을 추적하는 상태인지) 확인하기 위해 사용되는 명령어라 할 수 있다. 만약 파일의 상태가 untracked 라면 아직 파일을 하나도 수정하지 않았다는 의미이다. 따라서 untracked 상태는 파일들이 만들어지긴 했지만 만들어졌다는 사실만 알 뿐이다. git은 절대  untracked 상태 파일을 커밋하지 않는다. 그리고 status 명령어의 자주 사용할 것 같은 또 다른 옵션으로는 ‘git status -s' 가 있다. 이 옵션은 git status 명령으로 확인할 수 있는 내용을 좀 더 요약해서 보여준다.

![4](https://user-images.githubusercontent.com/80791532/117534293-adbf2680-b02b-11eb-8f68-fcb0fd70dc29.PNG)

## add
- 현재 문서는 untracked 상태(git이 파일을 추적하지 않는 상태)이다. 
- 이 상태에서 git이 파일을 추적하는 상태로 만들고 싶다.
- 이를 위해 git 명령어 ‘add’중에서도 ‘git add .' (현재 디렉토리의 모든 변경 내용을 staging area로 넘김) 명령어를 사용했다.
- 따라서 'add'명령어는 해당 파일을 staging area(커밋할 준비가 된 변경 내용이 Git 저장소에 기록되기 전에 대기하는 장소) 에 저장하여 Tracked 상태, 즉, git이 파일을 추적하고 관리하는 상태로 만들기 위해 사용하는 것으로 정리할 수 있다. 그리고 add 명령어의 자주 사용할 것 같은 또 다른 옵션으로는 ‘git add -A’와 ‘git add -p’ 가 있다. ‘git add -A’는 작업 디렉토리 내의 모든 내용을 몽땅 staging area로 넘기고 ‘git add -p’ 는 각 변경사항을 터미널에서 직접 눈으로 하나씩 확인하면서 staging area로 넘기거나 제외할 수 있다. 

![5](https://user-images.githubusercontent.com/80791532/117534317-cd564f00-b02b-11eb-8ab7-1f6bd4e4116e.PNG)

## commit
- 현재 문서는 tracked 상태이며 staging area에 저장되어 있다.
- 이 상태에서 파일을 git저장소에 저장하고 싶다.
- 이를 위해 git 명령어 ‘commit’ 중에서도 ‘git commit -m <커밋 메시지>’ 를 사용했다.(이때 커밋 메시지는 해당 작업이 무엇을 했는지를 잘 표현해야 한다)
- 따라서, ‘commit'명령어는 add 될 때의 파일의 상태를 git저장소에 저장하는 명령어라고 할 수 있다. 이때 git add 명령으로 추가하지 않은 파일은 커밋하지 않으며 Unstaged 상태의 파일은 커밋되지 않는다. 그리고 status 명령어의 자주 사용할 것 같은 또 다른 옵션으로는 ‘git commit -a’가 있다. 별도의 add명령어를 사용하지 않고도 수정된 파일에 대해 add명령과  commit명령을 한 번에 수행한다.

![6](https://user-images.githubusercontent.com/80791532/117534330-e232e280-b02b-11eb-927b-116485e70d99.PNG)

## log
- 현재 문서는 최초 커밋이 된 뒤에 문장의 수정이 이루어진 후 다시 한 번 커밋이 된 상태이다.
- 이 상태에서 git 저장소의 히스토리를 보고 싶다.
- 이를 위해 ‘log’ 명령어를 사용하였다.
- 따라서, ‘log’명령어는 git의 히스토리를 조회하여 저장소의 커밋 히스토리를 시간순으로 보여주는 명령어 라고 할 수 있다. 이때 가장 최근의 커밋이 가장 먼저 나온다. 그리고 log 명령어의 자주 사용할 것 같은 또 다른 옵션으로는 'git log -p'와 ‘git log --patch’ 가 있다. 'git log -p'와 ‘git log --patch’는 각 commit의 (변경사항)diff결과를 줄 단위로 보여준다. 따라서 동료가 무엇을 커밋했는지 빨리 조회하는데 유용하다.

![7](https://user-images.githubusercontent.com/80791532/117534350-f8d93980-b02b-11eb-96fe-a9c9f4a738f3.PNG)

## reset--hard
- 현재 문서는 문맥이 맞지 않는 문장을 수정한 뒤 다시 한 번 커밋이 이루어진 상태이다.
- 그러나 다시 보니 고치기 전 문장이 맞아서 고치기 전 상태로 만들고 이후의 커밋을 삭제하고 싶다.
- 이를 위해 'reset --hard' 명령어를 사용하였다.
- 따라서, 'reset --hard' 명령어는 과거의 커밋으로 돌아가고 해당 커밋 이후의 이력을 모두 삭제하는 명령어라고 할 수 있다. 그리고 reset 명령어의 자주 사용할 것 같은 또 다른 옵션으로는 ‘reset --soft’ 가 있다. reset --soft 옵션은 head와 branch 만 이동할 뿐 reset하기 전까지 했던 staging area, working directory의 작업은 남겨두어 git commit 을 했을 때 기존 상태로 돌아오게 된다. 따라서 ‘reset --soft’명령어는 과감한 'reset --hard'명령어와 달리 안전하고 신중한 옵션이라 할 수 있다.

![8](https://user-images.githubusercontent.com/80791532/117534381-21f9ca00-b02c-11eb-8a19-44e56a832c6a.PNG)

![9](https://user-images.githubusercontent.com/80791532/117534382-22926080-b02c-11eb-8a1c-79fd429d2d4f.PNG)

![10](https://user-images.githubusercontent.com/80791532/117534384-232af700-b02c-11eb-9b27-806f221cdf99.PNG)

## remote
- 현재 문서는 git에 의해 관리되고 있는 상태이다.
- 이 상태에서 원격 저장소(github의 repository)를 생성하여 다른 사람들과 협업할 수 있는 환경을 만들고 싶다.
- 이를 위해 'remote' 명령어를 사용하였다.
- 따라서, 이 remote 명령어는 github의 repository를 원격 저장소로 설정하기 위해 사용하는 것으로 정리할 수 있다. 그리고 remote 명령어의 자주 사용할 것 같은 또 다른 옵션으로는 git remote -v가 있다. remote -v 옵션을 주면 단축이름과 URL을 함께 볼 수 있다.

![11](https://user-images.githubusercontent.com/80791532/117534400-3938b780-b02c-11eb-9d42-f50f82b9749d.PNG)

## push
- 현재 아직 문서를 공유하고 있는 상태가 아니다.
- 이 상태에서 문서에 커밋된 내용들을 원격 저장소에 올려 다른 사람들과 협업하여 프로젝트를 진행하고 싶다.
- 이를 위해 'push' 명령어를 사용하였다.
- 따라서, 이 push 명령어는 local(컴퓨터)의 main 브랜치가 origin이라는 원격의 main을 추적하여 문서에 커밋된 내용들을 원격 저장소에 올리기 위해 사용하는 것으로 정리할 수 있다. 실제로 github을 새로 고침 해 보면 local에서 push 한 파일이 올라와 있고 어떤 커밋에서 마지막으로 생성되거나 변경되었는지도 나와 있다. 그리고 push 명령어의 자주 사용할 것 같은 또 다른 옵션으로는 'push -u'옵션이 있다. 이 옵션은 매번 저장소명과 브랜치명을 입력하지 않아도 최초에 한 번만 저장소명과 브랜치명을 입력하고 그 이후에는 모든 인자를 생략할 수 있다.

![12](https://user-images.githubusercontent.com/80791532/117534426-5cfbfd80-b02c-11eb-9875-9f34dcddec61.PNG)

## clone
- 컴퓨터로 하던 작업을 다른 컴퓨터로 옮겨와 작업을 이어가고 싶다.(가정)
- 이 상태에서 원격 저장소에 저장되어 있는 프로젝트를 통째로 내려받고 싶다.
- 이를 위해 'clone'명령어를 사용하였다.
- 따라서, 'clone'명령어는 처음 프로젝트에 투입되거나 다른 컴퓨터에서 새로 프로젝트를 다운받을 때 원격 저장소에 저장되어 있는 프로젝트(git repository 전체)를 현재 사용자의 로컬로 내려받는데 사용되는 명령어라고 할 수 있다. 그리고 clone 명령어의 자주 사용할 것 같은 또 다른 옵션으로는 'clone -b'옵션이 있다. 이 옵션은 브랜치 전체를 clone 하지 않고 특정 브랜치만 clone하는 것을 가능하게 해 준다.

![캡처](https://user-images.githubusercontent.com/80791532/117534638-4d30e900-b02d-11eb-995c-d0002bd21055.PNG)

## pull
- 현재 다른 팀원이 문서의 예제를 수정하여 커밋한 뒤 github에 업데이트 하였다.(가정)
- 이 상태에서 팀원이 수정한 내용을 클라이언트로 내려받고 싶다.
- 이를 위해 'pull'명령어를 사용하였다.
-  따라서, pull 명령어는 Github에서 다른 팀원이 코드를 업데이트했거나 Github를 통해서 commit했을 때 그 내용을 내려받는 명령어입니다. 그리고 pull 명령어의 자주 사용할 것 같은 또 다른 옵션으로는 'pull --ff-only'옵션이 있다. 이 옵션은 pull명령어를 실행할 때 기존에 존재하지 않는 commit이 생성되어 발생될 수 있는 문제를 방지하여 ‘pull --ff-only’ 옵션을 주어 실행하게 되면 fast-forwarded 가 새로운 commit 이 발생하지 않고 실행된다.

![14](https://user-images.githubusercontent.com/80791532/117534695-879a8600-b02d-11eb-95d7-5a270cf3603d.PNG)

## branch
- 현재 문서는 여러 팀원과 함께 협업하여 수정되고 있는 상태이다. 
- 이 상태에서 새로운 이미지를 테스트 해보고 싶지만 협업중인 문서를 함부로 변경할 수는 없으므로 독립적으로 어떤 작업을 테스트 해 볼 수 있는 상태로 만들고 싶다.
- 이를 위해 git 명령어 'branch'를 사용하였다.
- 따라서 'branch' 명령어는 기존의 'main' 브랜치에서 벗어나 독립적인 브랜치를 생성하여 새로운 브랜치에서 테스트나 작업을 수행할 수 있게 해주는 명령어라고 할 수 있다. 그리고 branch 명령어의 자주 사용할 것 같은 또 다른 옵션으로는 branch -d 와 branch -m 이 있다. branch -d는 로컬 브랜치를 삭제하는 옵션이고, branch -m은 브랜치명을 바꾸는 옵션이다.

![15](https://user-images.githubusercontent.com/80791532/117535949-5f158a80-b033-11eb-9668-edbf3ac0c430.PNG)

## checkout
- 현재 문서를 독립적으로 작업할 수 있는 branch를 새로 만들었지만 git은 아직 main 브랜치를 가리키고 있다.
- 이 상태에서 test branch로 이동하여 git이 test 브랜치를 가리키는 상태로 바꾸고 test 브랜치에서 이미지를 테스트 하고 싶다. 
- 이를 위해 'checkout' 명령어를 사용하였다.
- 따라서 'branch'명령어를 사용하여 새로운 브랜치를 만들었지만 'branch'명령어는 브랜치를 만들기만 하고 브랜치를 옮기지 않으므로 'checkout'명령어는 기본 main브랜치에서 원하는 브랜치로 이동하여 Git이 해당 브랜치를 가리키게 하는 역할을 하는 것으로 정리할 수 있다. 그리고 checkout 명령어의 자주 사용할 것 같은 또 다른 옵션으로는 checkout -b 가 있다. 이 옵션은 브랜치의 생성과 체크아웃을 한꺼번에 할 수 있게 해 준다.

![16](https://user-images.githubusercontent.com/80791532/117537316-fdf1b500-b03a-11eb-9f32-b149a5c4c065.PNG)

![17](https://user-images.githubusercontent.com/80791532/117537321-05b15980-b03b-11eb-8114-059788cfbf6b.PNG)

## merge
- 현재 문서는 독립적으로 작업할 수 있는 test 브랜치에서 테스트가 이루어지고 있다.
- 이 상태에서 test가 성공적으로 완료되었으므로 다시 원래의 main 브랜치에 적용하고 싶다.
- 이를 위해 'merge' 명령어를 사용하였다.
- 따라서 'merge'명령어는 다른 브랜치를 만들어 선택한 부분의 문제를 해결하고 다시 원래의 master 브랜치로 옮길 때 사용하는 것으로 정리할 수 있다. 이때 이전 다른 브랜치의 커밋이 master 커밋에 기반한 것이라면 merge과정 없이 그저 최신 커밋으로 이동한다. 이는 “Fast forward" 방식이라고 부른다. 그러나 master 브랜치와 별개로 진행되는 다른 브랜치라면 Git은 'Fast-forward’로 Merge 하지 않고 각 브랜치가 가리키는 커밋들과 공통 조상 하나를 사용하여 merge한다. 그리고 checkout 명령어의 자주 사용할 것 같은 또 다른 옵션으로는 merge --no-ff 와 merge --ff-only가 있다. merge --no-ff는  현재 브랜치와 병합 대상의 관계가 Fast-Forward이던 아니던 무조건 Merge 커밋과 같이 병합되는 옵션이고  merge --ff-only 는  현재 브랜치와 병합 대상의 관계가 Fast-Forward인 경우에만 병합을 진행하는 옵션이다.

![18](https://user-images.githubusercontent.com/80791532/117537641-4ca04e80-b03d-11eb-83ca-6e2da8b30b0c.PNG)

## rebase 
- 현재 문서는 새로운 idea 브랜치와 anotheridea 브랜치를 생성하였고 각각 idea브랜치에서는 새로운 아이디어의 수정이, anotheridea 브랜치에서는 코드의 수정이 이루어진 상태이다.
- 이 상태에서 새로운 merge commit을 남기지 않고 마치 다른 브랜치는 없었던 것처럼 프로젝트의 작업 내용을 하나의 흐름으로 유지하는 깔끔한 상태로 만들고 싶다.
- 이를 위해 'rebase'명령어를 사용하였다.
- 따라서 rebase명령어와 merge 명령어는 모두 합치는 역할을 하고 최종 결과물도 같지만 rebase 명령어는 merge 명령어보다 좀 더 깔끔한 히스토리를 만들때 사용하는 것으로 정리할 수 있다. Rebase 명령어의 경우는 브랜치의 변경사항을 순서대로 다른 브랜치에 적용하면서 합치기 때문이다. 그리고 rebase 명령어의 자주 사용할 것 같은 또 다른 옵션으로는 'rebase -i'가 있다. 이 옵션은 rebase 명령어를 대화형으로 실행하도록 해준다.

![19](https://user-images.githubusercontent.com/80791532/117541722-289a3880-b050-11eb-97b6-6594c118bb85.PNG)

## tag
- 현재 문서에서 문맥에 맞지 않는 부분을 찾아 수정하고 commit 한 상태이다.
- 이 상태에서 이 commit에 대해 tag(책갈피)를 붙이고 과거의 특정 commit에 대해서도 tag(책갈피)를 붙이고 싶다.
- 이를 위해 'tag'명령어를 사용합니다.
- 따라서, tag명령어는 현재 commit뿐만 아니라 과거의 commit을 넘나들며 이동할 수 있는 일종의 책갈피를 만들 때 사용하는 것으로 정리할 수 있다. 이때 tag는 수정이 불가능하며 읽기만 가능하다. 그리고 tag 명령어의 자주 사용할 것 같은 또 다른 옵션으로는 'tag -m' 이 있다. 이 옵션은 태그를 남길 때 메시지도 함께 남기도록 해준다.

![21](https://user-images.githubusercontent.com/80791532/117542503-dce98e00-b053-11eb-9460-25fea0b3125d.PNG)

![22](https://user-images.githubusercontent.com/80791532/117542514-e3780580-b053-11eb-8e41-0e7e8f81c9ac.PNG)

## 명령어/사용여부/링크

| 명령어 | [add](#add) | [branch](#branch) | [checkout](#checkout) | [clone](#clone) | [commit](#commit) | [config](#config) | [init](#init) | [log](#log) |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 사용여부 | O | O | O | O | O | O | O | O |

| 명령어 | [merge](#merge) | [pull](#pull) | [push](#push) | [rebase](#rebase) | [remote](#remote) | [reset--hard](#reset--hard) | [status](#status) | [tag](#tag) |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 사용여부 | O | O | O | O | O | O | O | O |

*링크 : 명령어를 클릭하면 해당 명령어 설명 부분으로 넘어갑니다.*


