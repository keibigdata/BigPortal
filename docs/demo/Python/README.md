# 주피터 노트북(노트북) 사용하기
## 분석환경 활용
- 서버접속: 주의사항(90일 암호변경)
- 개인환경 설정(virtualenv)
- 주피터랩 구성

### 개인 분석환경 설치 및 실행(종료)
- 설치할 위치에서 virtualenv [분석환경명] --python=[파이썬 바이너리]
- 사용가능한 파이썬 버전을 알고 싶은 경우에는 콘솔에서 python 입력 후 [탭] 키를 누르면 확인 가능
- 예를 들어, 분석환경명: p35_crawling, 파이썬 3.5를 사용할 경우 아래 예제를 참고
- 개인 분석환경을 활성화하려면, source [분석환경명]/bin/activate와 같이 입력
- 개인 분석환경을 나가려면, deactivate 입력
~~~
~@DA03:~$ python
python              python3             python3.6           python3.7m          python3m-config
python2             python3.5           python3.6-config    python3.8           python-config
python2.7           python3.5-config    python3.6m          python3-config
python2.7-config    python3.5m          python3.6m-config   python3-jsonschema
python2-config      python3.5m-config   python3.7           python3m
~@DA03:~$ virtualenv p35_crawling --python=python3.5
Running virtualenv with interpreter /usr/bin/python3.5
Using base prefix '/usr'
New python executable in /home/~/p35_crawling/bin/python3.5
Also creating executable in /home/~/p35_crawling/bin/python
Installing setuptools, pkg_resources, pip, wheel...done.
~@DA03:~$ source p35_crawling/bin/activate
(p35_crawling) ~@DA03:~$ deactivate
~~~
### 주피터랩 설치 및 실행
- 주피터랩 설치: pip install jupyterlab
- 실행: jupyter lab --ip=0.0.0.0 --port=[사번] &
- 작업 후 종료할 때는 fg 입력 후, Ctrl + C 키를 누르고 y로 종료(kill -9 [PID]로 종료 가능)
~~~
(p35_crawling) ~@DA03:~$ pip install jupyterlab
Collecting jupyterlab
  Downloading jupyterlab-2.3.1-py3-none-any.whl (7.9 MB)
     |████████████████████████████████| 7.9 MB 1.5 MB/s
(중략)
Installing collected packages: zipp, six, ipython-genutils, decorator, wcwidth, traitlets, pyrsistent, pyparsing, ptyprocess, parso, importlib-metadata, attrs, webencodings, tornado, pyzmq, python-dateutil, pygments, pycparser, prompt-toolkit, pickleshare, pexpect, packaging, MarkupSafe, jupyter-core, jsonschema, jedi, backcall, testpath, pandocfilters, nbformat, mistune, jupyter-client, jinja2, ipython, entrypoints, defusedxml, cffi, bleach, urllib3, terminado, Send2Trash, prometheus-client, nbconvert, ipykernel, idna, chardet, certifi, argon2-cffi, requests, notebook, json5, jupyterlab-server, jupyterlab
Successfully installed MarkupSafe-1.1.1 Send2Trash-1.5.0 argon2-cffi-20.1.0 attrs-20.3.0 backcall-0.2.0 bleach-3.3.0 certifi-2020.12.5 cffi-1.14.5 chardet-4.0.0 decorator-4.4.2 defusedxml-0.7.1 entrypoints-0.3 idna-2.10 importlib-metadata-2.1.1 ipykernel-5.5.0 ipython-7.9.0 ipython-genutils-0.2.0 jedi-0.17.2 jinja2-2.11.3 json5-0.9.5 jsonschema-3.2.0 jupyter-client-6.1.12 jupyter-core-4.6.3 jupyterlab-2.3.1 jupyterlab-server-1.2.0 mistune-0.8.4 nbconvert-5.6.1 nbformat-5.1.2 notebook-6.2.0 packaging-20.9 pandocfilters-1.4.3 parso-0.7.1 pexpect-4.8.0 pickleshare-0.7.5 prometheus-client-0.9.0 prompt-toolkit-2.0.10 ptyprocess-0.7.0 pycparser-2.20 pygments-2.8.1 pyparsing-2.4.7 pyrsistent-0.17.3 python-dateutil-2.8.1 pyzmq-20.0.0 requests-2.25.1 six-1.15.0 terminado-0.8.3 testpath-0.4.4 tornado-6.1 traitlets-4.3.3 urllib3-1.26.4 wcwidth-0.2.5 webencodings-0.5.1 zipp-1.2.0
(p35_crawling) b3nn9@DA03:~$ jupyter lab --ip=0.0.0.0 --port=8080 &
[1] 7703
(p35_crawling) ~@DA03:~$ [I 16:32:56.007 LabApp] JupyterLab extension loaded from /home/~/p35_crawling/lib/python3.5/site-packages/jupyterlab
[I 16:32:56.007 LabApp] JupyterLab application directory is /home/~/p35_crawling/share/jupyter/lab
[I 16:32:56.010 LabApp] Serving notebooks from local directory: /home/~
[I 16:32:56.010 LabApp] Jupyter Notebook 6.2.0 is running at:
[I 16:32:56.010 LabApp] http://a.b.c.d:x/?token=f
[I 16:32:56.010 LabApp]  or http://127.0.0.1:x/?token=f
[I 16:32:56.010 LabApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
[W 16:32:56.013 LabApp] No web browser found: could not locate runnable browser.
[C 16:32:56.014 LabApp]

    To access the notebook, open this file in a browser:
        file:///home/~/.local/share/jupyter/runtime/nbserver-7703-open.html
    Or copy and paste one of these URLs:
        http://a.b.c.d:x/?token=f
     or http://127.0.0.1:x/?token=f

^C[I 16:42:25.356 LabApp] interrupted
Serving notebooks from local directory: /home/~
0 active kernels
Jupyter Notebook 6.2.0 is running at:
http://a.b.c.d:x/?token=fb
 or http://127.0.0.1:x/?token=fb
Shutdown this notebook server (y/[n])? y
[C 16:42:27.018 LabApp] Shutdown confirmed
[I 16:42:27.019 LabApp] Shutting down 0 kernels
[I 16:42:27.019 LabApp] Shutting down 0 terminals
(p35_crawling) ~@DA03:~$
~~~
### 주피터랩 고급
- 매번 IP, 포트 넣는 것이 번거로울 때는 사전 설정 파일을 이용하는 것이 편리함
- 주피터랩이 설치된 상태에서 jupyter lab --generate-config 입력 후 설정파일은 편집
~~~
(nlp) ~@DA03:~$ cd
(nlp) ~@DA03:~$ jupyter lab --generate-config
Writing default config to: /home/~/.jupyter/jupyter_notebook_config.py
(nlp) ~@DA03:~$ vi ~/.jupyter/jupyter_notebook_config.py
(중략)
#c.NotebookApp.ip = 'localhost'
c.NotebookApp.ip = '0.0.0.0'
#c.NotebookApp.port = 8888
c.NotebookApp.port = [사번]
(중략)
(nlp) ~@DA03:~$ jupyter lab &
[1] 28803
(nlp) ~@DA03:~$ [I 16:57:15.427 LabApp] Writing notebook server cookie secret to /home/~/.local/share/jupyter/runtime/notebook_cookie_secret
[I 16:57:15.639 LabApp] JupyterLab extension loaded from /home/~/nlp/lib/python3.5/site-packages/jupyterlab
[I 16:57:15.639 LabApp] JupyterLab application directory is /home/~/nlp/share/jupyter/lab
[I 16:57:15.641 LabApp] Serving notebooks from local directory: /home/~
[I 16:57:15.642 LabApp] Jupyter Notebook 6.2.0 is running at:
[I 16:57:15.642 LabApp] http://a.b.c.d:x/?token=b
[I 16:57:15.642 LabApp]  or http://127.0.0.1:x/?token=b
[I 16:57:15.642 LabApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
[W 16:57:15.645 LabApp] No web browser found: could not locate runnable browser.
[C 16:57:15.645 LabApp]

    To access the notebook, open this file in a browser:
        file:///home/~/.local/share/jupyter/runtime/nbserver-28803-open.html
    Or copy and paste one of these URLs:
        http://a.b.c.d:10999/?token=b
     or http://127.0.0.1:10999/?token=b

(nlp) ~@DA03:~$ fg
jupyter lab
^C[I 16:57:28.732 LabApp] interrupted
Serving notebooks from local directory: /home/~
0 active kernels
Jupyter Notebook 6.2.0 is running at:
http://a.b.c.d:10999/?token=b
 or http://127.0.0.1:10999/?token=b
Shutdown this notebook server (y/[n])? y
[C 16:57:30.186 LabApp] Shutdown confirmed
[I 16:57:30.187 LabApp] Shutting down 0 kernels
[I 16:57:30.188 LabApp] Shutting down 0 terminals
(nlp) ~@DA03:~$
~~~
- 비밀번호도 설정 가능
- 예를 들어, 123456를 비밀번호로 설정하고 싶을 경우, 암호화된 비밀번호를 설정에 반영
- 여기까지 하면, 모든 개인환경에서 jupter lab & 만 사용 가능
~~~
(nlp) ~@DA03:~$ ipython
Python 3.5.10 (default, Feb 20 2021, 21:52:18)
Type 'copyright', 'credits' or 'license' for more information
IPython 7.9.0 -- An enhanced Interactive Python. Type '?' for help.

In [1]: from notebook.auth import passwd

In [2]: passwd()
Enter password:
Verify password:
Out[2]: 'argon2:$'

In [3]: exit
(nlp) ~@DA03:~$ vi ~/.jupyter/jupyter_notebook_config.py
(중략)
#c.NotebookApp.password = ''
c.NotebookApp.password = 'argon2:$'     
(중략)
(nlp) ~@DA03:~$ jupyter lab &
[1] 36417
(nlp) ~@DA03:~$ [I 17:05:04.526 LabApp] JupyterLab extension loaded from /home/~/nlp/lib/python3.5/site-packages/jupyterlab
[I 17:05:04.526 LabApp] JupyterLab application directory is /home/~/nlp/share/jupyter/lab
[I 17:05:04.528 LabApp] Serving notebooks from local directory: /home/~
[I 17:05:04.528 LabApp] Jupyter Notebook 6.2.0 is running at:
[I 17:05:04.528 LabApp] http://a.b.c.d:x/
[I 17:05:04.528 LabApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
[W 17:05:04.532 LabApp] No web browser found: could not locate runnable browser.
[I 17:05:38.588 LabApp] 302 GET / (1.2.3.4) 1.190000ms
[I 17:05:38.606 LabApp] 302 GET /lab? (1.2.3.4) 1.230000ms
[I 17:05:42.263 LabApp] 302 POST /login?next=%2Flab%3F (1.2.3.4) 54.420000ms
[W 17:05:42.980 LabApp] Could not determine jupyterlab build status without nodejs

(nlp) ~@DA03:~$ fg
jupyter lab


^C[I 17:05:53.640 LabApp] interrupted
Serving notebooks from local directory: /home/noconda
0 active kernels
Jupyter Notebook 6.2.0 is running at:
http://a.b.c.d:x/
Shutdown this notebook server (y/[n])? y
[C 17:05:54.938 LabApp] Shutdown confirmed
[I 17:05:54.938 LabApp] Shutting down 0 kernels
[I 17:05:54.939 LabApp] Shutting down 0 terminals
(nlp) noconda@DA03:~$
~~~
