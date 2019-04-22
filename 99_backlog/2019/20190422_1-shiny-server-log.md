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
