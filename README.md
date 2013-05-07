android_local_razrqcom
======================

Local Manifest for Cyanogenmod 10.1 on Motorola Razr Qcom devices

Getting Started
---------------

To get started with Android, you'll need to get
familiar with [Git and Repo](http://source.android.com/download/using-repo).

Make a build directory:

	mkdir Andoid (or whatever name you choose)
	cd Android (or the name  you chose)
	mkdir .repo/local_manifests

To initialize your local repository using the Cyanogemod manifest, use commands like these:

    repo init -u git://github.com/CyanogenMod/android.git -b cm-10.1

    curl -L -o .repo/local_manifests/razrqcom.xml -O -L https://raw.github.com/razrqcom-dev-team/android_local_razrqcom/cm-10.1/razrqcom.xml
 
    	( or Download: https://github.com/razrqcom-dev-team/android_local_razrqcom/blob/cm-10.1/razrqcom.xml
		and place it in ~/Android/.repo/local_manifest.xml (or ~/'name you chose'/.repo)

Then to sync up:

    repo sync
