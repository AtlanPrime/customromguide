* Device sources aka Trees

So, you probably downloaded the rom sources and set your git id. Well the next step is to find your device sources (Device Tree , Kernel Tree , Vendor Tree {And A Common Tree if available for both vendor and device})

* The prerequisites are:

- to know your device code name
- to know what platform it is (would make it easier to find the common trees)
- to know if the trees are readily avialable (for most xiaomi/oneplus/etc.. devices its a true case scenario)
- to clone them to your github account so that u can do a bringup of the tree for the ROM

Here is an example device ( Redmi Note 6 Pro )

> Code Name: tulip, SoC: Snapdragon 636, Platform: SDM660

Here, the common tree for tulip is sdm660-common (this exists for thr vendor too). 
Also, the trees are avialable in the following orgs
- https://GitHub.com/Xiaomi-SDM660 
- https://GitHub.com/Xiaomi-SDM660-Devs

Now, tulip is not the only device with the SDM660 platform. 
Devices like Whyred (Redmi Note 5/Pro), Wayne/Jasmine (Mi 6x/Mi A2) etc are also belonging to the SDM660 Platform. 
The only thing u need to be aware of is the manufacturer because motorola, nokia, etc.. also has SDM660 Platform devices..

Examples of Other Platforms are SDM660 SM6150 SM6250 SM8150 SM8250 SD845 etc...
