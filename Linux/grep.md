# [LINUX] grep으로 텍스트 문서에서 데이터 뽑아내기.

2틀간의 AWS SUMMIT을 다녀오고 나서 오랜만에 일을 다시 하려고 했다.

마지막으로 작업한 부분을 다시 체크해 보려고 하고 있는데...

이상한 데이터를 발견 했다. 그래서 서버에 들어가 Log파일을 보려고 하는데...

몇일간의 데이터가 계속 쌓여 있다 보니  `vi`로 데이터를 보는것에 한계를 느끼고

바로 구글링 시작. 

`bash`에서 데이터를 볼수 있는 방법을 찾았고 그 사용법을 기록해 둔다. 

``` bash
grep -n "찾을 데이터" "파일명"

//  EX
grep -n "XX.XXX.XX.XX" access.log 
2790241:XX.XXX.XX.XX - - [20/Apr/2017:05:27:28 +0900] ...
2790242:XX.XXX.XX.XX - - [20/Apr/2017:05:27:29 +0900] ...
2790244:XX.XXX.XX.XX - - [20/Apr/2017:05:27:30 +0900] ...
2790245:XX.XXX.XX.XX - - [20/Apr/2017:05:27:31 +0900] ...
2790246:XX.XXX.XX.XX - - [20/Apr/2017:05:27:31 +0900] ...
2790248:XX.XXX.XX.XX - - [20/Apr/2017:05:27:32 +0900] ...
2790249:XX.XXX.XX.XX - - [20/Apr/2017:05:27:33 +0900] ...

```