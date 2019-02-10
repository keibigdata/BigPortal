### 환경구성 시 오류
- 파이썬 버전 2에서는 특수문자 경로가 있는 경우 오류가 발생할 수 있다.  
  (되도록 파이썬 버전 3을 사용하자.)  
~~~
b3nn9@DataLX01:~/문서/+환경 빅데이터 분석플랫폼(Big Portal)/51_코드리뷰/Vector-based navigation using grid-like representations in artificial agents$ virtualenv env
Running virtualenv with interpreter /usr/bin/python2
New python executable in /home/b3nn9/문서/+환경 빅데이터 분석플랫폼(Big Portal)/51_코드리뷰/Vector-based navigation using grid-like representations in artificial agents/env/bin/python2
Also creating executable in /home/b3nn9/문서/+환경 빅데이터 분석플랫폼(Big Portal)/51_코드리뷰/Vector-based navigation using grid-like representations in artificial agents/env/bin/python
Traceback (most recent call last):
  File "<string>", line 1, in <module>
UnicodeDecodeError: 'ascii' codec can't decode byte 0xeb in position 12: ordinal not in range(128)
ERROR: The executable /home/b3nn9/문서/+환경 빅데이터 분석플랫폼(Big Portal)/51_코드리뷰/Vector-based navigation using grid-like representations in artificial agents/env/bin/python2 is not functioning
ERROR: It thinks sys.prefix is u'/home/b3nn9/\ubb38\uc11c/+\ud658\uacbd \ube45\ub370\uc774\ud130 \ubd84\uc11d\ud50c\ub7ab\ud3fc(Big Portal)/51_\ucf54\ub4dc\ub9ac\ubdf0/Vector-based navigation using grid-like representations in artificial agents' (should be u'/home/b3nn9/\ubb38\uc11c/+\ud658\uacbd \ube45\ub370\uc774\ud130 \ubd84\uc11d\ud50c\ub7ab\ud3fc(Big Portal)/51_\ucf54\ub4dc\ub9ac\ubdf0/Vector-based navigation using grid-like representations in artificial agents/env')
ERROR: virtualenv is not compatible with this system or executable
~~~
  (파이썬 버전 3의 예)  
~~~
b3nn9@DataLX01:~/문서/+환경 빅데이터 분석플랫폼(Big Portal)/51_코드리뷰/Vector-based navigation using grid-like representations in artificial agents$ virtualenv --python=python3.5 env
Running virtualenv with interpreter /usr/bin/python3.5
Using base prefix '/usr'
New python executable in /home/b3nn9/문서/+환경 빅데이터 분석플랫폼(Big Portal)/51_코드리뷰/Vector-based navigation using grid-like representations in artificial agents/env/bin/python3.5
Also creating executable in /home/b3nn9/문서/+환경 빅데이터 분석플랫폼(Big Portal)/51_코드리뷰/Vector-based navigation using grid-like representations in artificial agents/env/bin/python
Installing setuptools, pkg_resources, pip, wheel...done.
b3nn9@DataLX01:~/문서/+환경 빅데이터 분석플랫폼(Big Portal)/51_코드리뷰/Vector-based navigation using grid-like representations in artificial agents$ source env/bin/activate
(env) b3nn9@DataLX01:~/문서/+환경 빅데이터 분석플랫폼(Big Portal)/51_코드리뷰/Vector-based navigation using grid-like representations in artificial agents$ deactivate
b3nn9@DataLX01:~/문서/+환경 빅데이터 분석플랫폼(Big Portal)/51_코드리뷰/Vector-based navigation using grid-like representations in artificial agents$ 
~~~
