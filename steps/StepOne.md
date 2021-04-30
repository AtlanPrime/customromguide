#Set Up a Build Environment

* A) The Way I do..


```bash
# get superuser access.
sudo su

# install JDK 
add-apt-repository ppa:openjdk-r/ppa

# update all packages.
apt-get update

# install Java packages.
apt-get install git-core gnupg flex bison build-essential zip curl zlib1g-dev gcc-multilib g++-multilib libc6-dev-i386 lib32ncurses5-dev x11proto-core-dev libx11-dev lib32z1-dev libgl1-mesa-dev libxml2-utils xsltproc unzip fontconfig

# become a normal user.
exit

# creating a bin folder and setting up AkhilNarang Script.

mkdir ~/bin

PATH=~/bin:$PATH

cd ~/bin

curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo

chmod a+x ~/bin/repo

git clone https://github.com/akhilnarang/scripts.git scripts

cd scripts

bash setup/android_build_env.sh
```

* B) The AOSP way to do..

https://source.android.com/setup/build/initializing
