kzhiquan-blog
=============
A simple static blog, which is based on markdown and python(tornado).
Thanks to MartianZ, the blog source code is brought from [him](https://github.com/MartianZ).


## dependancy ##
	
	python2.7
	easy_install
	virtualenv
	easy_install tornado
	easy_install markdown
	easy_install PyRSS2Gen
	easy_install pycrypto

## build ##
1. Download source code: git clone git@github.com:kzhiquan/kzhiquan-blog.git;
2. Construct virtual env for python running: virtualenv env;
3. Active local python runtime env: source ./env/bin/activate;
4. Install dependancy packages: tornado, markdown, PyRSS2Gen, pycrypto;
5. Start blog: python blog.py;
6. All of aboved cmd operation is understand directory: kzhiquan-blog;
7. Access blog on local url: http://localhost:8888/;

## deployment ##
1. Run the webservice forever: nohup python blog.py &;
2. Produce ssh-key on VPS: ssh-keygen -t rsa;
3. Copy ssh-key to Github: /root/.ssh/id_rsa.pub;
4. Install Git on Ubuntu: apt-get update; apt-get install git-core;
5. Install python dev env, for example: easy_install:sudo apt-get install python-setuptools python-dev build-essential;
6. Install virtualenv: easy_install virtualenv;
7. Stop apache2 server: sudo /etc/init.d/apache2 stop;

