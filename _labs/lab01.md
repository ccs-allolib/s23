---
desc: Getting Started
assigned: 2023-04-10 9:30
due: 2023-04-12 10:45
layout: default
num: lab01
ready: false
signup_app: https://ucsb-cs-github-linker.herokuapp.com/
slack: https://allolib-s23.slack.com
course_org: https://github.com/allolib-s23
course_org_name: allolib-s23
starter_repo: https://github.com/AlloSphere-Research-Group/allolib_playground
prefix: demo1
---


This assignment is `lab01`

If you find typos or problems with the lab instructions, please report
them on the `#help-lab01` channel on Slack

# Goals

This lab checks that you can succesfully create a piece using the techniques shown in the file `tutorials/01_SineEnv.cpp` in the repo <{{page.starter_repo}}>.




## Step 1: Cloning the demo1 repo on your machine


1. Create a directory somewhere on your machine for your work this quarter, and change directory into it.  You might called it `allolib` for example, but the name is up to you.
   
   ```
   mkdir ~/allolib
   cd ~/allolib
   ```

   (As mentioned above, you can actually use any directory you like; but we suggest this approach.  We'll refer
   to `~/allolib` throughout the rest of
   the instructions for consistency.)

2. Now, go to the this webpage:
  
   * <https://github.com/orgs/allolib-s23/repositories>
   
   and find your `demo1-userid` repo. The page should look something like this:

   <img width="761" alt="image" src="https://user-images.githubusercontent.com/1119017/230951970-b2f40853-73c8-4375-97d5-c957b8bfb76d.png">


   Select your own repo, and you should see something like this:
   
   <img width="1211" alt="image" src="https://user-images.githubusercontent.com/1119017/230952087-f205ebf8-a5ca-4358-ab0d-403d32d57f8d.png">


   You should see a button for `SSH`;
   select that button.  Then there is a button to copy the URL shown;
   click that to copy the URL.

3. Now type this command, replacing
   `url` with the url that you copied.

   That `url` should be something like
   <tt>git@github.com:{{page.course_org_name}}/{{page.prefix}}-cgaucho.git</tt> but with your GitHub id in place of <tt>cgaucho</tt>.

   ```
   git clone url
   ```

   You'll will see a warning message that you are cloning an empty repo; that's normal.

   
   <tt>Cloning into {{page.prefix}}-cgaucho...<br />
   warning: You appear to have cloned an empty repository<br /></tt>
   
  
4. If you use the `ls` command, you should now have a subdirectory called <tt>{{page.prefix}}-cgaucho</tt> (except <tt>cgaucho</tt> will be your GitHub username.)  Use
   a `cd` command to change directory 
   into that directory, e.g.

   
   <tt>cd {{page.prefix}}-cgaucho</tt>
   

   An `ls -a` should reveal an empty
   directory except for the `.git` subdirectory indicating that this is a GitHub repo.  

   ```
   % ls -a
   .	..	.git
   % 
   ```

   We are now ready to pull in some starter code.


## Step 2: A remote for the starter code (allolib_playground)

The Allolib Playground repo is here: <{{page.starter_repo}}>

If you've used `git` before, you
may be familiar with the command:

```
git pull origin master
```

The word `origin` in this case refers to a *remote*, that is a repo that lives somewhere out there on the network.   

The word `master` refers to the default branch of the repo.  The default branch of GitHub repos recently changed from `master` to `main`; we'll be using `main` throughout this course.

If you type the following command, you'll see that `origin` is defined as a remote for the repo that you cloned from.  Your output will look similar, except that you'll have your GitHub in place of `cgaucho`:

<tt>
% git remote -v<br />
origin	git@github.com:{{page.course_org_name}}/{{page.prefix}}-cgaucho.git (fetch)<br />
origin	git@github.com:{{page.course_org_name}}/{{page.prefix}}-cgaucho.git (push)<br />
% <br />
</tt>

Now, we are going to add a second remote.  This remote will use the URL for the starter code.

The image below shows how to copy that URL: (1) Click the green `Code` button.  (2) Select `SSH` to choose that as the network protocol for the URL (3) Click the icon to copy the URL to your clipboard.



Then, use this command to add a remote called `allolib-playground` for the starter code repo:


* <tt>git remote add allolib-playground {{page.starter_repo}}</tt>


After this command, use `git remote -v` to list all your remotes. Your output should look like this (except your GitHub id in place of `cgaucho`):

<tt>
% git remote -v<br />
origin	git@github.com:{{page.course_org_name}}/{{page.prefix}}-cgaucho.git (fetch)<br />
origin	git@github.com:{{page.course_org_name}}/{{page.prefix}}-cgaucho.git (push)<br />
allolib-playground	git@github.com:AlloSphere-Research-Group/allolib_playground.git (fetch)<br />
allolib-playground	git@github.com:AlloSphere-Research-Group/allolib_playground.git (push)<br />
% 
</tt>

## Step 3: Pull Starter Code into your Repo

The next step is to pull the starter code into your repo, and then push
that code to your origin repo on GitHub.

Here are the three commands:

```
git checkout -b master
git pull allolib-playground master
git push origin master
```

After these three commands, go look at your repo on GitHub, i.e. the repo at this url (but substituting your GitHub id for cgaucho:)

* <https://github.com/{{page.course_org_name}}/{{page.prefix}}-cgaucho>

You should see that instead of an empty repo, you now have a copy of the `allolib_playground` starter code.


## Step 4: Run the 01_SineEnv.cpp demo. 

Then: 
* If you haven't already done it, set up the preliminaries needed for Allolib: Follow the instructions here for your platform: <https://github.com/AlloSphere-Research-Group/allolib/blob/master/readme.md>
* Follow the instructions for getting started with Allolib-Playground: <https://github.com/AlloSphere-Research-Group/allolib_playground>
* Try running the Sine Wave demo:
  ```
  ./run.sh tutorials/synthesis/01_SineEnv.cpp
  ```

## Step 5: Make your own!

Copy the 01_SineEnv.cpp demo (or any other file to s23_demo1.cpp.

Now you can start playing with making your own creation!


