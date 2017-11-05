AospExtended For Xiaomi Redmi 4A
================================

Initializing:

First, create a folder to hold the source code: 

	mkdir ~/aex

Next, naviate into that new directory via the terminal:

	cd ~/aex

To initialize your local repository use this command:

	repo init -u git://github.com/AospExtended/manifest.git -b 7.x

Also add the local manifests:

	git clone https://github.com/Xiaomi-MSM8937/local_manifest -b aex-n .repo/local_manifests

Then sync up with this command:

	repo sync -c -jx --force-sync --no-clone-bundle --no-tags
	
You can make the 4 higher depending on how fast your internet connection is. 

-------------
 
_Building from source_
---------------

First:

	cd ~/aex
Second:

	$ echo "export USE_CCACHE=1" >> ~/.bashrc
	$ prebuilts/misc/linux-x86/ccache/ccache -M 50G

Third:

	. build/envsetup.sh
  	lunch aosp_rolex-userdebug
	maka aex -j8
