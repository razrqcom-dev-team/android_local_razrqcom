android_local_razrqcom
======================

Local Manifest for Motorola Razr Qcom devices

Getting Started
---------------

To get started with Android, you'll need to get
familiar with [Git and Repo](http://source.android.com/download/using-repo).

Make a build directory:

	mkdir Andoid (or whatever name you choose)
	cd Android (or the name  you chose)
	

To initialize your local repository using the Cyanogemod manifest, use commands like these:

    repo init -u git://github.com/CyanogenMod/android.git -b cm-10.1

    curl -L -o .repo/local_manifest.xml -O -L https://raw.github.com/razrqcom-dev-team/android_local_razrqcom/master/local_manifest.xml
 
    	( or Download: https://github.com/razrqcom-dev-team/android_local_razrqcom/blob/master/local_manifest.xml
		and place it in ~/Android/.repo/local_manifest.xml (or ~/'name you chose'/.repo)

Then to sync up:

    repo sync

You will need to know how to do some cherry-picks:

http://review.cyanogenmod.org/#/c/28192/ Init: Allow building of init that is compatible with second init boot

http://review.cyanogenmod.org/#/c/28195/ PhoneProxy: On v6 or greater RIL, when LTE_ON_CDMA is TRUE
