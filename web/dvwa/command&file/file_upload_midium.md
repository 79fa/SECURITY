Midium 의 경우 low 와 다르게 .php 파일을 올리지 못하게 되어 있다.   
그래서 hack.php.png이렇게 저장을 한다면 올라간다.   
그 후 command injection을 이용해 파일 이름을 바꿔준 후 url으 이동시키면 된다.   


먼저 command injection으로 가서 그곳의 위치르 확인한다. 
![ㅁㄴㅇㄹ](https://github.com/79fa/SECURITY/blob/main/images/스크린샷%202021-07-23%20오후%203.01.10.png)
두번 위로 올라간 후에 hackable/uploads로 가면 hack.php.png이 있을 것이라느 것을 알 수 있다. 

mv ../../hackable/uploads/hack.php.png ../../hackable/uploads/hack1.php 를 하면 파일 이름이 바뀌고   
url을 바꾸면 코드가 실행이 되는 것을 알 수 있다.  

![asdf](https://github.com/79fa/SECURITY/blob/main/images/스크린샷%202021-07-23%20오후%203.04.07.png)



