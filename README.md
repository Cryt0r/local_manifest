DotOS For Xiaomi Redmi 4A
=========================

Initializing:

First, create a folder to hold the source code: 

	mkdir ~/DotOS

Next, naviate into that new directory via the terminal:

	cd ~/DotOS

To initialize your local repository use this command:

	repo init -u git://github.com/DotOS/manifest.git -b dot-n

Also add the local manifests:

	git clone https://github.com/Xiaomi-MSM8937/local_manifest -b dot-n .repo/local_manifests

Then sync up with this command:

	repo sync -f -j8 --force-sync --no-clone-bundle
	
You can make the 4 higher depending on how fast your internet connection is. 

-------------
 
_Building from source_
---------------

First:

	cd ~/DotOS

Second:

	$ echo "export USE_CCACHE=1" >> ~/.bashrc
	$ prebuilts/misc/linux-x86/ccache/ccache -M 50G

Third:

	. build/envsetup.sh
	brunch rolex
