# How to setup jupyterhub

```
sudo apt install -y nodejs
sudo apt install npm
sudo npm install -g configurable-http-proxy
sudo pip3 install jupyter
sudo pip3 install jupyterhub
sudo pip3 install jupyterlab
mkdir jupyter-notebook
jupyterhub --generate-config

# set on jupyter-conf.py
c.JupyterHub.admin_users = set(["admin"])




# install supervisor
sudo apt-get install -y supervisor


# go to /etc/supervisor/conf.d/conf.jupyterhub.conf


####

[program:jupyterhub]
command = jupyterhub --ssl-key /path/to/cert/jhub.key --ssl-cert /path/to/cert/jhub.crt --port 443 -f /path/to/config/jupyterhub_config.py
autostart=true
autorestart=true
stopasgroup=true
killasgroup=true


####


sudo supervisorctl reread
sudo supervisorctl update

sudo supervisorctl

```





# jupyter extension

```
sudo pip3 install jupyterlab-system-monitor
sudo pip3 install jupyter-tensorboard


sudo pip3 install jupyterlab_latex
sudo pip3 install lckr-jupyterlab-variableinspector
```
