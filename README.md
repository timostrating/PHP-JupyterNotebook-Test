# PHP-JupyterNotebook-Test
This is a quick test to see if i can get a PHP kernel working in Jupyter.
 
# 1 - Installing Jupyter with the php kernel

## Ubuntu 16.04 (this probably works on any version of ubuntu)
**Requirements**

1. Install Jupyterlab ```$ pip install jupyterlab``` *(requires python and pip)* -- more info on jupyterLab can be found here: https://github.com/jupyterlab/jupyterlab
1. Install composer *(requires php)* https://getcomposer.org/download/

**Now we are ready to install the php jupyter kernel.**

1. Make sure you have php also installed as cli ```$ sudo apt install php-cli``` this probably already the case.
1. Go to https://litipk.github.io/Jupyter-PHP-Installer/ (requires PHP >= 7.0) and click on "Download .PHAR installer".
	1. The php ZMQ extension is also required ```$ sudo apt-get install php-zmq```
1. Now run the installer we downloaded ```$ php ./jupyter-php-installer.phar install```
1. restart / start Jupyterlab and we are done ```$ jupyter lab```

## Windows 10
I did not got it working on my windows machine. I will update this readme as soon as I do get it working. 
It has to do with the php ZMQ extension that needs to be manualy installed on windows. (Stackoverflow is telling me that you should download the dll versions of the extension you want to install. This dll should than be moved in your php installation folder. After moving the file there you should also add it to your php.ini file to make it really working. )



# 2 - Setting up the enviorment for the more advanced examples.

## pchart on Ubuntu 16.04 (this probably works on any version of ubuntu)

We are using [pchart](http://www.pchart.net/) in our notebook. Pchart requires you to install the gd and truetype extensions. Remember that you can only install the php 7 versions of extensions in the case you want to use a extension with the jupyter php kernel.

```$ sudo apt-get install php7.0-gd``` 

```$ sudo apt-get install freetype*``` <-- this wildcard is here to install the tools and the demos

Pchart uses UTF8 functions to correct the output. Only not all php functions that help with UTF8 are in php 7.0 So we need to get the old php 5 functions working as well. So we neet to install this extension as well.

```$ sudo apt-get install php7.0-xml``` <-- UTF8 functions from php 5

