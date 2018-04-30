# PHP-JupyterNotebook-Test
This is a quick test to see if i can get a PHP kernel working in Jupyter.
 

## Ubuntu 16.04 (this probably works on any version of ubuntu)
**Requirements**

1. Install Jupyterlab ```pip install jupyterlab``` *(requires python and pip)* -- more info on jupyterLab can be found here: https://github.com/jupyterlab/jupyterlab
1. Install composer *(requires php)* https://getcomposer.org/download/

**Now we are ready to install the php jupyter kernel.**

1. Make sure you have php also installed as cli ```sudo apt install php-cli``` this probably already the case.
1. Go to https://litipk.github.io/Jupyter-PHP-Installer/ (requires PHP >= 7.0) and click on "Download .PHAR installer".
	1. The php ZMQ extension is also required ```sudo apt-get install php-zmq```
1. Now run the installer we downloaded ```php ./jupyter-php-installer.phar install```
1. restart / start Jupyterlab and we are done ```jupyter lab```

## Windows 10
I did not got it working on my windows machine. I will update this readme as soon as I do get it working. 
It has to do with the php ZMQ extension that needs to be manualy installed on windows.
