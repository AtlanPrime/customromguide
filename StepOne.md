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
apt-get install bison build-essential curl ccache flex lib32ncurses5-dev lib32z1-dev libesd0-dev libncurses5-dev libsdl1.2-dev libxml2 libxml2-utils lzop pngcrush schedtool squashfs-tools xsltproc zip zlib1g-dev git-core make phablet-tools gperf openjdk-8-jdk

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
