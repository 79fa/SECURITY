message   부분에 내용을 넣은 후에 scipt로 이루어진 구문을 넣는다.    
abc<script>alert("XSS Atack")</script>   
이렇게 할시 abc만 저장이 되고 스크립트에 <script>alert("XSS Atack")</script>  이부분을 저장할 수 있다. 
웹이 저 곳을 실행하여 하면 alert로 인해 XSS Atack 가 뜨게 된다. 

![이미지2](https://github.com/79fa/SECURITY/blob/main/images/스크린샷%202021-07-22%20오후%204.15.44.png)


