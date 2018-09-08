## 윈도우 환경에서 분석플랫폼 활용하기
  
### 포트포워딩
- 
~~~
D:\>netsh interface portproxy add v4tov4 listenport=50764 listenaddress=0.0.0.0 connectport=7640 connectaddress=192.168.1.50


D:\>netsh interface portproxy add v4tov4 listenport=51764 listenaddress=0.0.0.0 connectport=764 connectaddress=192.168.1.51


D:\>netsh interface portproxy add v4tov4 listenport=51888 listenaddress=0.0.0.0 connectport=8000 connectaddress=192.168.1.51


D:\>netsh interface portproxy show all

ipv4 수신 대기:             ipv4에 연결:

주소            포트        주소            포트
--------------- ----------  --------------- ----------
0.0.0.0         50764       192.168.1.50    7640
0.0.0.0         51764       192.168.1.51    764
0.0.0.0         51888       192.168.1.51    8000


D:\>
~~~
- 참고 : [Windows에서 포트포워딩(Port Forwarding) 설정하기)](https://www.tuwlab.com/ece/29011)
