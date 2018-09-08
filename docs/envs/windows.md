## 윈도우 환경에서 분석플랫폼 활용하기
### 포트포워딩
-
~~~
C:\Users\KEI>netsh interface portproxy add v4tov4 listenport=50764 listenaddress=0.0.0.0 connectport=7640 connectaddress=192.168.1.50
~~~
- 참고 : [Windows에서 포트포워딩(Port Forwarding) 설정하기)](https://www.tuwlab.com/ece/29011)
