## bof5번 문제 


![image](https://github.com/79fa/SECURITY/blob/main/스크린샷%202021-07-15%20오후%205.23.20.png?raw=true)   
  3,4번과 같은 방법을 이용해서 buf와 값을 입력받는 곳 사이의 바이트를 구한다.   
  140이라는 수가 나왔고 140후에는 innocent 에 값이 저장이 될 것이라는 것을 알 수 있다. 




![image](https://github.com/79fa/SECURITY/blob/main/스크린샷%202021-07-15%20오후%205.26.50.png?raw=true)
코드를 보면 4번과 다른 점이 system() 안에 /bin/sh 가 들어 있지 않고 buf가 들어 있다는 것이다.   
buf 에 /bin/sh를 넣어 주어야 한다. 하지만 그냥 넣으면 뒤에 의미 없는 값들과 innocent에 넣고자 한 값들까지 들어갈 수 있음으로 null 을 넣어서 끊어준다. 
null을 보면 문자열이 끝났다고 판단을 한다. 


![image](https://github.com/79fa/SECURITY/blob/main/스크린샷%202021-07-15%20오후%205.24.29.png?raw=true).  
  /bin/sh와 \x00을 합치면 8바이트가 나오고 나머지 132바이트를 의미 없는 값으로 채운 후 innocent값을 넣으면 된다. 



