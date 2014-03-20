---
layout: post
title: The Fastest Way to Create Install and Deploy a Ruby on Rails App in Five Minutes - 最快速度 5 分钟内创建、安装、部署、上线 Rails 应用
---

#The Fastest Way to Create Install and Deploy a Ruby on Rails App in Five Minutes


## Buy Mac


## Install

### Binaries

#### XCode

* [http://itunes.apple.com/us/app/xcode/id497799835?mt=12](http://itunes.apple.com/us/app/xcode/id497799835?mt=12)
* [https://developer.apple.com/downloads/](https://developer.apple.com/downloads/)

#### GCC

* [https://github.com/kennethreitz/osx-gcc-installer](https://github.com/kennethreitz/osx-gcc-installer)

#### MySQL

* [http://dev.mysql.com/downloads/mysql/](http://dev.mysql.com/downloads/mysql/)

#### MacPorts

* [http://www.macports.org/install.php](http://www.macports.org/install.php)

___
    sudo port selfupdate
    sudo port install memcached ImageMagick

### Ruby

    \curl -L https://get.rvm.io | bash -s head --ruby
    rvm install 2

### Rails

    gem install rails -v 4.1.0.rc1


## Create

    git clone https://yourname@github.com/yourname/project.git
    rails new project
    cd project/


## Coding

### Generate controllers

    rails g controller Users index new create edit update destroy

### Generate models

    rails g model User email:string encrypted_password:stirng lock_verion:integer

### Initailize database

    rake db:create
    rake db:migrate
    rake db:seed

### Editing

    mate .

###

    ...........
    ...
    ....
    ..
    .
    .
    ........................................ # deadline night

### Source control

    git add --all
    git diff # code review
    git commit
    git push


## Deploy

### Buy VPS

### Install CentOS 6.5

### Install Ruby

### Rails app

    yum install git-core
    cd /opt/
    git clone https://yourname@github.com/yourname/project.git
    cd project/
    bundle
    vi config/database.yml
    vi config/secrets.yml
    rake db:create RAILS_ENV=production
    rake db:migrate RAILS_ENV=production
    rake db:seed RAILS_ENV=production
    rake assets:precompile RAILS_ENV=production
    rails s -eproduction

### Daemon services

#### Thin

    thin install
___
    vi /etc/thin/project.yml # https://gist.github.com/swordray/9423884
<script src="https://gist.github.com/swordray/9423884.js"></script>
    /etc/init.d/thin restart

#### Nginx

    yum install nginx
___
    vi /etc/nginx/config/project.conf
<script src="https://gist.github.com/swordray/8882089.js"></script>
    nginx -s reload
