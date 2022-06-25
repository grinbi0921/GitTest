저장소(폴더)의 생성 : git init
>>폴더생성과 유사한 개념으로 지금은 이해하고있다

만든 저장소(폴더)에 파일 추가 : git add 파일명(git_command.txt)
>>폴더에 추가되긴하지만, 빨간색으로 표시되며 아직 git에 반영되지않은 상태를 의미

저장소(폴더)에 반영 : git commint
>>반영하는 파일이 초록색으로 변경되며 git에 반영됨

git상황을 확인 : git status

※ 마지막 리눅스의 vim 에디터로 표시되며
i -> 파일명(git_command.txt) -> ESC -> : -> wq

기존 파일을 변경후 저장할겨우, commit단계 조심
git commit -m "update git_command.txt"
>>"update git_command.txt"은 업데이트 명을 지정해준것인듯.

수정한 내용을 보려면  : git log
>>윗쪽이 가장 최신의 내용으로 표시된다.
log를 좀더 시작적으로 확인하려면 gitk라는 명령어로 가능하다.

현재 저장소에 어떤 branch가 존재하는지 확인 : git branch
>>branch는 현재 작업상태에서 복사하여 새로운 분활된 저장소를 만들어주는 명령어
>>처음에는 ★master만 보이며 ★의 의미는 현재 선택이되어있는 branch를 의미함

새로운 branch를 생성 : git branch 브렌치명
>> git branch test1 (아무런 반응없음)

기본 branch에서 새로운 branch로 선택권을 이동
git checkout test1  <-> 반대로 master로 돌아가기위해 : git checkout master

///현재 이파일의 작업시점은 test1 branch에 존재하는 파일입니다.///
test1이라는 branch에서 변경한 내용을 병합하기위해 master branch로 이동하여, 
git merge test1
>>test1에서 변경한 내용들이 master branch에 병합된다.
>>병합된 branch는 더이상 필요가 없기에, git branch -d test1(d옵션은 삭제)

**********************************************************************************
test1의 branch의 내용을 모두 수정한 다음 master branch에서 병합하기전에 
master branch의 내용이 수정된다면, commit에는 같은 파일의 수정 내용이 두개가 존재하여 충돌이 발생

both modified git_command.txt라는 메세지가 뜬다.

이럴때는 파일을 열어서 양쪽파일들의 충돌이 발생하지않도록 수정하고, add 한후 다시한번 commit한다. 
**********************************************************************************

원격저장소로 활용하기 위해서 표준처럼 github를 사용한다.
우선, github에 로그인하고 repository를 생성하거나 이미 생성된 repository의 오른쪽 code에서 주소를 복사해서
내 컴퓨터의 콘솔에서 원격저장소(repository)를 생성할 경로로 이동하여 clone라는 명령어로 github에서 만든 원격저장소를 복사해온다
※ 저는 기존 local에서 만들어놓은 저장소가 있다면, 그 저장소(폴더)안으로 콘솔에서 작업해보자
완료되면 github에서 만들었던 repository가 폴더형태로 복사된 것을 확인할수있다.








