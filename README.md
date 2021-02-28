

## 構成

`web client` <-> `web server(nginx)` <-> `socket` <-> `uWSGI` <-> `Python(django)`

## 起動方法

前提としてnginxが起動していること。
ローカルの場合、nginxは8000でlistenさせて、指定したソケットに向けてプロキシさせていること。


`uwsgi --socket rate_apps.sock --wsgi-file rate_apps/wsgi.py --chmod-socket=666`



## Postgreについて

### 起動

`pg_ctl -D postgres start`


### 停止

`pg_ctl -D postgres stop`
