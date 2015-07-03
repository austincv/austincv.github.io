---
layout: post
title: Setting up this blog
---

Thanks to the excellent work done by Barry, getting this up and running was easier than I thought.
For more instructions head over to the [Jekyll Now repository](https://github.com/barryclark/jekyll-now) on GitHub.

## Setting up Jekyll on Windows 8

I usually do all my work on Linux but I thought why not give a try on windows
There was this other nice [website](http://jekyll-windows.juthilo.com/) which
made setting up Jekyll to serve the website locally a pleasure.
The following is what I did to set my environment on my Windows 8

### Install Python

You need python pigments for syntax highlighting. So you need to install and add python to your path. 
The actual install of pigments will be taken care of by gem install github-pages later on.
I got the python installer from [here](https://www.python.org/downloads/)
I went with Python 2.7.10 as I wasn't sure of compatibility with 3.x.x 

- [Python 2.7.10](https://www.python.org/ftp/python/2.7.10/python-2.7.10.msi)

Don't forget to include it in your path during the installation

![Add to path](/images/add_python_path2.PNG "Click on the red X and select Will be installed on local hard drive")

### Install Jekyll

For this you need ruby. At the point of writing this the latest Ruby version available was Ruby 2.2.2. 
I chose the x64 bit versions. Download the latest versions available [here](http://rubyinstaller.org/downloads/)

The following are the links to the ones that I downloaded:

- [Ruby](http://dl.bintray.com/oneclick/rubyinstaller/rubyinstaller-2.2.2-x64.exe)
- [Ruby Dev Kit](http://dl.bintray.com/oneclick/rubyinstaller/DevKit-mingw64-64-4.7.2-20130224-1432-sfx.exe)

Make sure that the Ruby and the Ruby Dev Kit versions are compatible.
It's written on the [downloads](http://rubyinstaller.org/downloads/) page which one goes with which version.

The is a self-extracting archive. When you execute the file, it’ll ask you for a destination for the files. 
Enter a path that has no spaces in it like ```C:\RubyDevKit\```  and Click Extract and wait until the process is finished.

Next, you need to initialize the DevKit and bind it to your Ruby installation. 
Open the command prompt and type the following replace C:\RubyDevKit with the path that you provided while extracting.

```
cd C:\RubyDevKit
ruby dk.rb init
ruby dk.rb install
```

Now you are all set to install Jekyll.
There is a ruby gem that takes care of that.
Type the following command and it should install jekyll and the plug-ins used by GitHub Pages.

```
gem install github-pages
```

Now we are ready to clone our git repo and start posting 

### Install GitHub for Windows

This is straight forward. Head over to [this page](https://windows.github.com/) and download the latest version of 
GitHub available and Install it.

Open GitHub and clone your repo. I have cloned it to ```Documents\GitHub\```

![git clone ](/images/gitclone.png "Click on the +, move to Clone tab and click on your repo and Clone")

Now you are all set to serve your website locally
Open up the command prompt and type the following.
 
Remember to change ```C:\Users\Austin\Documents\GitHub\austincv.github.io``` with the path where you have put your repository

```
cd C:\Users\Austin\Documents\GitHub\austincv.github.io
jekyll serve
```

You are all set.
Open up your favourite web browser and go to [http://localhost:4000](http://localhost:4000)

Now you can edit your posts and view it on your local machine before pushing to GitHub