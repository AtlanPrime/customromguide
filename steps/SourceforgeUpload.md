# Upload to Sourceforge

At first go to the rom output directory where the zip is present so that it is easier to upload from there
ex:
```bash
[baby@linux ~]$ cd rom/out/target/product/devicename
* here if you do ls you can see the rom zip if compiled fully!
```
Secondly go to [SourceForge](https://sourceforge.net/) and create an account as well as a new project. Make sure you remember your 
  * "Username: Your SourceForge.net Username" and 
  * "Password: Your SourceForge.net Password"

An example session might look like (where Username="baby", Project UNIX name="babyproject",Release dir is "folder1"):

*Type in the following according to your username, project name, folder name
```bash
[baby@linux ~]$ sftp baby@frs.sourceforge.net
Connecting to frs.sourceforge.net...
The authenticity of host 'frs.sourceforge.net (216.34.181.57)' can't be established.
RSA key fingerprint is 68:b3:26:02:a0:07:e4:78:d4:ec:7f:2f:6a:4d:32:c5.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added 'frs.sourceforge.net,216.34.181.57' (RSA) to the list of known hosts.
jsmith@frs.sourceforge.net's password:
sftp> cd /home/frs/project/babyproject/folder1
sftp> put rom.zip
Uploading rom.zip to /home/frs/project/babyproject/folder1/rom.zip
rom.zip                                                                                       100%  241     30.2MB/s   00:51
sftp> exit
```

* i.e First type
```bash
sftp baby@frs.sourceforge.net
```
* When asked for "Are you sure you want to continue connecting" type in "yes"
* Type in your password when asked
* You will be seeing this now
```bash
Connected to frs.sourceforge.net.
sftp>
```
* Now cd into your project location
 ```bash
 cd /home/frs/project/babyproject/
* here after the projectname you can add the folder name or else it'll directly be uploaded into the project root
```
* Now type put followed by the rom.zip name
 ```bash
sftp> put rom.zip
Uploading rom.zip to /home/frs/project/babyproject/rom.zip
rom.zip                                                                                       100%  241     30.2MB/s   00:51
sftp> exit
```

There! Now you have uploaded your ROM to SF.
It might take up to 10 Min to show up on the SF server.
Be patient.. Enjoy!!
