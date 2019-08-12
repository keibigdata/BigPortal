# pip install nltk -U
~~~
Looking in indexes: http://ftp.daumkakao.com/pypi/simple
Collecting nltk
  Downloading http://mirror.kakao.com/pypi/packages/87/16/4d247e27c55a7b6412e7c4c86f2500ae61afcbf5932b9e3491f8462f8d9e/nltk-3.4.4.zip (1.5MB)
     |████████████████████████████████| 1.5MB 1.0MB/s
Requirement already satisfied, skipping upgrade: six in /usr/local/lib/python3.6/dist-packages (from nltk) (1.11.0)
Building wheels for collected packages: nltk
  Building wheel for nltk (setup.py) ... done
  Created wheel for nltk: filename=nltk-3.4.4-cp36-none-any.whl size=1451035 sha256=7da9fa74faaf7b11848e89d3b73aea0c6d3e4b4882f3d7bd50b726e47a668fba
  Stored in directory: /root/.cache/pip/wheels/3b/50/68/ea7f253ce973d45987a3c2ab357ae42421335a0fa8d59020a7
Successfully built nltk
Installing collected packages: nltk
  Found existing installation: nltk 3.3
    Uninstalling nltk-3.3:
      Successfully uninstalled nltk-3.3
Successfully installed nltk-3.4.4
root@DataLX01:~# pip install konlpy -U
Looking in indexes: http://ftp.daumkakao.com/pypi/simple
Requirement already up-to-date: konlpy in /usr/local/lib/python3.6/dist-packages (0.5.1)
Requirement already satisfied, skipping upgrade: JPype1>=0.5.7 in /usr/local/lib/python3.6/dist-packages (from konlpy) (0.6.3)
~~~
# pip install gensim -U
~~~
Looking in indexes: http://ftp.daumkakao.com/pypi/simple
Collecting gensim
  Downloading http://mirror.kakao.com/pypi/packages/40/3d/89b27573f56abcd1b8c9598b240f53c45a3c79aa0924a24588e99716043b/gensim-3.8.0-cp36-cp36m-manylinux1_x86_64.whl (24.2MB)
     |████████████████████████████████| 24.2MB 1.2MB/s
Requirement already satisfied, skipping upgrade: scipy>=0.18.1 in /usr/local/lib/python3.6/dist-packages (from gensim) (1.1.0)
Collecting smart-open>=1.7.0 (from gensim)
  Downloading http://mirror.kakao.com/pypi/packages/37/c0/25d19badc495428dec6a4bf7782de617ee0246a9211af75b302a2681dea7/smart_open-1.8.4.tar.gz (63kB)
     |████████████████████████████████| 71kB 74.1MB/s
Requirement already satisfied, skipping upgrade: numpy>=1.11.3 in /usr/local/lib/python3.6/dist-packages (from gensim) (1.16.2)
Requirement already satisfied, skipping upgrade: six>=1.5.0 in /usr/local/lib/python3.6/dist-packages (from gensim) (1.11.0)
Requirement already satisfied, skipping upgrade: boto>=2.32 in /usr/local/lib/python3.6/dist-packages (from smart-open>=1.7.0->gensim) (2.48.0)
Requirement already satisfied, skipping upgrade: requests in /usr/local/lib/python3.6/dist-packages (from smart-open>=1.7.0->gensim) (2.18.4)
Requirement already satisfied, skipping upgrade: boto3 in /usr/local/lib/python3.6/dist-packages (from smart-open>=1.7.0->gensim) (1.7.12)
Requirement already satisfied, skipping upgrade: certifi>=2017.4.17 in /usr/local/lib/python3.6/dist-packages (from requests->smart-open>=1.7.0->gensim) (2018.11.29)
Requirement already satisfied, skipping upgrade: urllib3<1.23,>=1.21.1 in /usr/local/lib/python3.6/dist-packages (from requests->smart-open>=1.7.0->gensim) (1.22)
Requirement already satisfied, skipping upgrade: idna<2.7,>=2.5 in /usr/local/lib/python3.6/dist-packages (from requests->smart-open>=1.7.0->gensim) (2.6)
Requirement already satisfied, skipping upgrade: chardet<3.1.0,>=3.0.2 in /usr/local/lib/python3.6/dist-packages (from requests->smart-open>=1.7.0->gensim) (3.0.4)
Requirement already satisfied, skipping upgrade: jmespath<1.0.0,>=0.7.1 in /usr/local/lib/python3.6/dist-packages (from boto3->smart-open>=1.7.0->gensim) (0.9.3)
Requirement already satisfied, skipping upgrade: botocore<1.11.0,>=1.10.12 in /usr/local/lib/python3.6/dist-packages (from boto3->smart-open>=1.7.0->gensim) (1.10.12)
Requirement already satisfied, skipping upgrade: s3transfer<0.2.0,>=0.1.10 in /usr/local/lib/python3.6/dist-packages (from boto3->smart-open>=1.7.0->gensim) (0.1.13)
Requirement already satisfied, skipping upgrade: docutils>=0.10 in /usr/local/lib/python3.6/dist-packages (from botocore<1.11.0,>=1.10.12->boto3->smart-open>=1.7.0->gensim) (0.14)
Requirement already satisfied, skipping upgrade: python-dateutil<3.0.0,>=2.1; python_version >= "2.7" in /usr/local/lib/python3.6/dist-packages (from botocore<1.11.0,>=1.10.12->boto3->smart-open>=1.7.0->gensim) (2.7.0)
Building wheels for collected packages: smart-open
  Building wheel for smart-open (setup.py) ... done
  Created wheel for smart-open: filename=smart_open-1.8.4-cp36-none-any.whl size=73428 sha256=4878c4322f3f241c025efa3507466d122fec0712396509220d290240360f04df
  Stored in directory: /root/.cache/pip/wheels/d0/3a/ec/ddca7c66ed6d16d4416fc75c470385945066d1f0b6b7b366a7
Successfully built smart-open
Installing collected packages: smart-open, gensim
  Found existing installation: smart-open 1.5.7
    Uninstalling smart-open-1.5.7:
      Successfully uninstalled smart-open-1.5.7
  Found existing installation: gensim 3.1.0
    Uninstalling gensim-3.1.0:
      Successfully uninstalled gensim-3.1.0
Successfully installed gensim-3.8.0 smart-open-1.8.4
~~~
# pip install twython -U
~~~
Looking in indexes: http://ftp.daumkakao.com/pypi/simple
Collecting twython
  Downloading http://mirror.kakao.com/pypi/packages/8c/2b/c0883f05b03a8e87787d56395d6c89515fe7e0bf80abd3778b6bb3a6873f/twython-3.7.0.tar.gz
Requirement already satisfied, skipping upgrade: requests>=2.1.0 in /usr/local/lib/python3.6/dist-packages (from twython) (2.18.4)
Collecting requests_oauthlib>=0.4.0 (from twython)
  Downloading http://mirror.kakao.com/pypi/packages/c2/e2/9fd03d55ffb70fe51f587f20bcf407a6927eb121de86928b34d162f0b1ac/requests_oauthlib-1.2.0-py2.py3-none-any.whl
Requirement already satisfied, skipping upgrade: certifi>=2017.4.17 in /usr/local/lib/python3.6/dist-packages (from requests>=2.1.0->twython) (2018.11.29)
Requirement already satisfied, skipping upgrade: idna<2.7,>=2.5 in /usr/local/lib/python3.6/dist-packages (from requests>=2.1.0->twython) (2.6)
Requirement already satisfied, skipping upgrade: urllib3<1.23,>=1.21.1 in /usr/local/lib/python3.6/dist-packages (from requests>=2.1.0->twython) (1.22)
Requirement already satisfied, skipping upgrade: chardet<3.1.0,>=3.0.2 in /usr/local/lib/python3.6/dist-packages (from requests>=2.1.0->twython) (3.0.4)
Collecting oauthlib>=3.0.0 (from requests_oauthlib>=0.4.0->twython)
  Downloading http://mirror.kakao.com/pypi/packages/05/57/ce2e7a8fa7c0afb54a0581b14a65b56e62b5759dbc98e80627142b8a3704/oauthlib-3.1.0-py2.py3-none-any.whl (147kB)
     |████████████████████████████████| 153kB 1.0MB/s
Building wheels for collected packages: twython
  Building wheel for twython (setup.py) ... done
  Created wheel for twython: filename=twython-3.7.0-cp36-none-any.whl size=40512 sha256=603d0429c8d38b77facb568979e863b0a7ec3f4549ab85678d48672d9cdcaa51
  Stored in directory: /root/.cache/pip/wheels/76/fe/47/658c2d76f79f7e291a7c0fc2185b30e837d75dedb46aa9dee6
Successfully built twython
Installing collected packages: oauthlib, requests-oauthlib, twython
  Found existing installation: oauthlib 1.0.3
    Uninstalling oauthlib-1.0.3:
      Successfully uninstalled oauthlib-1.0.3
Successfully installed oauthlib-3.1.0 requests-oauthlib-1.2.0 twython-3.7.0
~~~
