---
layout: post
title: Termux Vscode setting_1
date: 15-07-2024
categories: [vscode]
tag: [like, comment, subscribe]
---

![kido](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fsyskido%2Fhit-counter&count_bg=%2379C83D&title_bg=%23555555&icon=accusoft.svg&icon_color=%23E7E7E7&title=나령윤기도&edge_flat=false)

# Welcome to Termux
> 
> Docs:       https://doc.termux.com
> Community:  https://social.termux.com
> Termux vscode 설치방법
> Working with packages:
>  Search:  pkg search <query>
>  Install: pkg install <package>
>  Upgrade: pkg upgrade



#  pkg install pulseaudio
> ~~~ $ ls
> Test  storage  syskido.github.io  tset
> ~ $ cd Test/
> ~/Test $ ls
> README.md
> ~/Test $ vim README.md
> ~/Test $ git init
> Reinitialized existing Git repository in /data/data/com.termux/files/home/Test/.git/
> ~/Test $ git status
> On branch main
> Your branch is up to date with 'origin/main'.~~ 

> ~~~/Test $ git add .
> ~/Test $ git commit -m 'first'
> [main a0dcee4] first
>  1 file changed, 3 insertions(+), 1 deletion(-)
>  ~~
> ~/Test $ git remote add origin https://github.com/syskido/Test.git

# error: remote origin already exists.
> ~~~/Test $ git config --global user.name 'syskido'
> ~/Test $ git config --global user.email 'syskido82@gmail.com'
> ~/Test $ git remote add origin https://github.com/syskido/Test.git
> error: remote origin already exists.~~


~/Test $ git remote add origin https://github.com/syskido/Test.git
error: remote origin already exists.
~/Test $ git remote remove origin
~/Test $ git remote add origin https://github.com/syskido/Test.git
~/Test $ git push origin master
error: src refspec master does not match any
error: failed to push some refs to 'https://github.com/syskido/Test.git'


~/Test $ git push origin main
Username for 'https://github.com': syskido
Password for 'https://syskido@github.com':
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see

  https://docs.github.com/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for 'https://github.com/syskido/Test.git/'
~/Test $ git push origin main
Username for 'https://github.com': syskido
Password for 'https://syskido@github.com':
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see

  https://docs.github.com/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for 'https://github.com/syskido/Test.git/'
~/Test $ git push origin main
Username for 'https://github.com': syskido
Password for 'https://syskido@github.com':
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 292 bytes | 292.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/syskido/Test.git
   e5a5237..a0dcee4  main -> main
   
   
~/Test $ pkg remove game-repo
Note, selecting 'apt' instead of 'game-repo'
Summary:
  Upgrading: 0, Installing: 0, Removing: 0, Not Upgrading: 0
~/Test $ pkg remove science-repo
Note, selecting 'apt' instead of 'science-repo'
Summary:
  Upgrading: 0, Installing: 0, Removing: 0, Not Upgrading: 0~~
  
# ~/Test $ 
# apt update
> ~~Hit:1 https://termux.net stable InRelease
> All packages are up to date.

> /Test $ apt install proot-distro
> proot-distro is already the newest version (4.14.1).
> Summary:
>   Upgrading: 0, Installing: 0, Removing: 0, Not Upgrading: 0~~
  
  
# ~/Test $ 
# proot-distro install ubuntu
> ~~[*] Installing Ubuntu (24.04)...
> [*] Creating directory '/data/data/com.termux/files/usr/var/lib/proot-distro/installed-rootfs/ubuntu'...
> [*] Creating directory '/data/data/com.termux/files/usr/var/lib/proot-distro/installed-rootfs/ubuntu/.l2s'...
> [*] Creating directory '/data/data/com.termux/files/usr/var/lib/proot-distro/dlcache'...
> [*] Downloading rootfs tarball...
> [*] URL: https://github.com/termux/proot-distro/releases/download/v4.11.0/ubuntu-noble-aarch64-pd-v4.11.0.tar.xz
> 
>   % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
>                                  Dload  Upload   Total   Spent    Left  Speed
>   0     0    0     0    0     0      0      0 --:--:-- -  0     0    0     0    0     0      0      0 --:--:-- -  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0
>   1 23.7M    1  303k    0     0   269k      0  0:01:30  100 23.7M  100 23.7M    0     0  14.0M      0  0:00:01  0:00:01 --:--:-- 41.4M
> 
> [*] Checking integrity, please wait...
> [*] Extracting rootfs, please wait...
> [*] Writing file '/data/data/com.termux/files/usr/var/lib/proot-distro/installed-rootfs/ubuntu/etc/environment'...
> [*] Updating PATH in '/data/data/com.termux/files/usr/var/lib/proot-distro/installed-rootfs/ubuntu/etc/bash.bashrc' if needed...
> [*] Updating PATH in '/data/data/com.termux/files/usr/var/lib/proot-distro/installed-rootfs/ubuntu/etc/profile' if needed...
> [*] Updating PATH in '/data/data/com.termux/files/usr/var/lib/proot-distro/installed-rootfs/ubuntu/etc/login.defs' if needed...
> [*] Creating file '/data/data/com.termux/files/usr/var/lib/proot-distro/installed-rootfs/ubuntu/etc/resolv.conf'...
> [*] Creating file '/data/data/com.termux/files/usr/var/lib/proot-distro/installed-rootfs/ubuntu/etc/hosts'...
> [*] Registering Android-specific UIDs and GIDs...
> [*] Running distribution-specific configuration steps...
> Generating locales (this might take a while)...
>   en_US.UTF-8... done
> Generation complete.
> [*] Finished.
> 
> Log in with: proot-distro login ubuntu
> 
#  ~/Test $~~


<script src="https://utteranc.es/client.js"
        repo="syskido/syskido.github.io"
        issue-term="pathname"
        theme="github-dark-orange"
        crossorigin="anonymous"
        async>
</script>        
        
        
        
        
