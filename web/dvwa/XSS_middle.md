script가 먹지 않아 image 방법을 시도했다.   
message에는 안먹도 name 에는 길이가 안됐다.   
개발자도구를 이용하여 name이 받아올 수 있는 길이를 늘리고   
\<img src="#" onerror="alert('XSS Atack')"> 을 넣으니 \<img src="#" onerror="alert('XSS Atack')"> 이부분이 스크립트에 저장이 되었다.   
![이니](https://github.com/79fa/SECURITY/blob/main/images/스크린샷%202021-07-22%20오후%205.06.11.png)

