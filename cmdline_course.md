---
layout: default
---

## Course Description

This course is an introduction to command line use both for basic everyday tasks and text processing. The course can be completed fully online, but live sessions and Slack-chat were a huge help during this adventure. I am also grateful for additional material on topics with a lot of very useful links to different online courses and other resources, a lot of them end up in my bookmarks and plans for future endeavours in Linux world.

Though I like digital note-taking but found that an old-school small paper notebook for writing down commands and their specifications worked best for me as I did not need to switch apps while watching or reading study material. Of course I will transfer everything to digital as soon as I have some spare time between other courses.

## Week 1 Introduction to Command Line Environments

This was an easy start for me as I did not need any additional preparations to get to a command line. Moreover, I have already done some small stuff using it.

We started with some pretty basic commands for everyday use. I knew some of them, but the need to repeat them for dozens of times during videos and tasks actually engraved them in me 😄 Tab and arrows use saved me a lot of typing (and nerves) for the whole course duration.

Incomplete list of studied commands:
- `pwd`
- `ls` and `tree`
- `cd`
- `mv` and `cp`
- `cat` and `less`
- `nano`
- `mkdir`
- `rm` and `rmdir`
- `wget`

... and a bunch of ways of quitting programs or processes.


## Week 2 Navigating a UNIX System

It was mostly about permissions. Finally I understood the numbers YouTube bloggers were throwing when speaking about permissions and why it is so important in Linux. Though number system is shorter I prefer to use letters with `chmod`, less possibilities to mess up.

Some basic info about process handling that I still do not comprehend much (mostly because I do not need to force kill processes on my machine) but at least I have notes 😄

Remote access via ssh was the scariest part! But it went surprisingly smoothly with a bit of confusion from shadow password input. But google is free 😄 Now I need only to input `ssh puhti` into the terminal and try not to mistype the password that I made unnecessary long.

Directory compression though understandable is still a bit messy (I just forget to `cd ..` before doing it).

## Week 3 Basic Corpus Processing

Now we are finally starting doing actual linguistic operations. I learned a lot about different encoding systems reading additional materials. The need of `doc2unix` was a surprise. I am happy Linux can do converting without additional fuzz. In Windows GUI it is not that easily done.

We were introduced to pipelines `|` and some essential text processing commands:
- `tr`
- `sort`
- `uniq`
- `wc`

And of course `grep` and `egrep` beasts of regular expressions. REs are cool and all but boy was it confusing. The printed cheatsheet was my hero during assignments and I still use it!

## Week 4 Advanced Corpus Processing

This week was about `sed`. I am still afraid of using it as am not confident in my knowledge. It is a rather complicated command this numbers of operators.

The most needed commands are:
- `'s/PATTERN/RESULT/' OLDFILE > NEWFILE` to get a file with changes made
- `'/PATTERN/d'` to delete the pattern
- `'/PATTERN/p'` to print lines with the pattern
- `-r` turns on regular expressions
- `-n` omit lines without the pattern
- if `g` is added after last / - include everything (only the first match is the default)

Looks easy but it was the lowest score for week assignment for me.

## Week 5 Scripting and Configuration Files

This week was fun! I love making my work more efficient. Scripts are all about this exact thing.

Though I like how my bash prompt looks like I experimented a bit with .bashrc. Not everything worked but I did not bother to google the problems. Surely I will research when I actually need to change the prompt appearance.

I like the clear error messages as I often forget to add some attributes. That is why I include them in every script in the assignment 😄

```
#!/bin/bash
if [ $# -ne 1 ]     # for error message about lack of an argument
then
  echo "ERROR: Input an adjective as an argument to proceed"
  exit 1
fi
echo $1'er'
```

Also, if script has loops it is nice to receive a message the work is done!

```
#!/bin/bash
file=$1  # needed file as the first attribute
if [ $# -ne 1 ]     # for error message about lack of a filename
then
  echo "ERROR: Input a filename to read"
  echo "$0 file_to_read"
  exit 1
fi
while read -r line
do
  echo $line
done < "$file"
echo "Task completed"     # just a satisfaction from a work done

```

A lot of ideas for automation but too little actual knowledge yet. Searching for additional tutorials is inevitable 😄

## Week 6 Installing and Running Programs

First of all, I need this alias 😄
![alt text](link to image)

This was a familiar topic as I use Linux for a while now. But I needed to take into account that my Fedora uses `yum` or `dnf` instead of `apt` so additional search and modifications of the commands.

`sudo dnf update` and `sudo dnf install PACKEGENAME`

Python virtual environments were a new concept.

`python -m venv VENVNAME` - to create a vertual envoronment

`sourse VENVNAME/Scripts/activate` - to activate it

## Week 7 Version Control

## Final Project GitHub Pages

All edits were done in KWrite, a default text editor in KDE Plazma.
