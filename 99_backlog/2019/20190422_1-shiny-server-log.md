## Shiny Server 로그 설정
- access_log 설정
~~~
~:/etc/shiny-server$ sudo vi shiny-server.conf
$ sudo systemctl restart shiny-server.service
~~~
~~~
$ cat shiny-server.conf
# Instruct Shiny Server to run applications as the user "shiny"
run_as shiny;

# https://docs.rstudio.com/shiny-server/#server-log
# combined, common, short, tiny, dev
access_log /var/log/shiny-server/access.log combined;

# Define a server that listens on port 3838
server {
  listen 3838;

  # Define a location at the base URL
  location / {

    # Host the directory of Shiny Apps stored in this directory
    site_dir /srv/shiny-server;

    # Log all Shiny output to files in this directory
    log_dir /var/log/shiny-server;

    # When a user visits the base URL rather than a particular application,
    # an index of the applications available in this directory will be shown.
    directory_index on;
  }
}
~~~
~~~
......
::ffff:192.168.110.52 - - [22/Apr/2019:02:24:05 +0000] "GET /odm/dt-core-1.10.16/css/jquery.dataTables.extra.css HTTP/1.1" 200 240 "http://data01.kei.re.kr:3838/odm/" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/73.0.3683.103 Safari/537.36"
::ffff:192.168.110.52 - - [22/Apr/2019:02:24:05 +0000] "GET /odm/dt-core-1.10.16/js/jquery.dataTables.min.js HTTP/1.1" 200 - "http://data01.kei.re.kr:3838/odm/" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/73.0.3683.103 Safari/537.36"
::ffff:192.168.110.52 - - [22/Apr/2019:02:24:05 +0000] "POST /odm/session/2fa81afe32d277a610696bdb37cd5051/dataobj/r1?w=&nonce=b6b8a92007435ae4 HTTP/1.1" 200 - "http://data01.kei.re.kr:3838/odm/" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/73.0.3683.103 Safari/537.36"
::ffff:192.168.110.52 - - [22/Apr/2019:02:24:06 +0000] "POST /odm/session/2fa81afe32d277a610696bdb37cd5051/dataobj/r1?w=&nonce=b6b8a92007435ae4 HTTP/1.1" 200 - "http://data01.kei.re.kr:3838/odm/" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/73.0.3683.103 Safari/537.36"
~~~
