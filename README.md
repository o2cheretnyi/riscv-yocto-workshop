Workshop prerequisites

We would recommend you to install Ubuntu 18.04 LTS on your computer or use preferable virtual machine environment
(e.g. VirtualBox) with Ubuntu 18.04 LTS installed on it to practice on current workshop (approx. 50GB disk space, 4GB RAM).

We have to download some cached data to save a time before the workshop starts, so enter your preferable terminal
and type next commands:

~$ sudo apt-get update

~$ sudo apt-get install python binutils chrpath cpp diffstat g++ gcc liblz4-tool make zstd libc-dev-bin python3-setuptools curl git gawk git-lfs

~$ mkdir -p workspace/{yocto,bin} && cd workspace/yocto

~/workspace/yocto$ curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ../bin/repo

~/workspace/yocto$ chmod +x ../bin/repo

\~/workspace/yocto$ echo "export PATH=\~/workspace/bin:$PATH" >> ~/.bashrc ; source ~/.bashrc

~/workspace/yocto$ repo init -u https://github.com/o2cheretnyi/riscv-yocto-workshop.git -b main -m yocto-workshop.xml
# takes approx. 3 minutes
~/workspace/yocto$ repo sync
# takes approx. 7 minutes
~/workspace/yocto$ git -C workshop-download lfs pull cache
# takes approx. 20 minutes
~/workspace/yocto$ git -C workshop-sstate lfs pull cache
