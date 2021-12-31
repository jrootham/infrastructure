# Infrastructure

## Reverse Proxy

Nginx is used as a reverse proxy for backend servers.  It translates https messages from the internet and translates them to an http message to the approprate port on localhost.

In the nginx config I need to add:

location /server1path 
{
    proxy_pass http://127.0.0.1:8000;
}

location /server2path 
{
    proxy_pass http://127.0.0.1:8001;
}

etc.

## Controlling Servers

We need to control (bring up, take down, reload) the server processes.  I believe we have 2 choices: systemd and service control.

### Systemd

### Service Control


