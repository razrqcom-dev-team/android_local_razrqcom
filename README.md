android_local_razrqcom
======================

Local Manifest for KitKat on Motorola msm8226 devices

Getting Started
---------------

To get started with Android, you'll need to get
familiar with [Git and Repo](http://source.android.com/download/using-repo).

Make a build directory:

	mkdir Andoid (or whatever name you choose)
	cd Android (or the name  you chose)
	mkdir .repo/local_manifests

To initialize your local repository using the CyanogenMod manifest, use commands like these:

    repo init -u git://github.com/CyanogenMod/android.git -b cm-11.0

    curl -L -o .repo/local_manifests/msm8226.xml -O -L https://raw.github.com/razrqcom-dev-team/android_local_razrqcom/msm8226-kk/msm8226.xml
 
    	( or Download: https://github.com/razrqcom-dev-team/android_local_razrqcom/blob/msm8226-kk/msm8226.xml
		and place it in ~/Android/.repo/local_manifest.xml (or ~/'name you chose'/.repo)

To sync the vendor files:

    curl -L -o .repo/local_manifests/vendor.xml -O -L https://raw.github.com/razrqcom-dev-team/android_local_razrqcom/msm8226-kk/vendor.xml
 
    	( or Download: https://github.com/razrqcom-dev-team/android_local_razrqcom/blob/msm8226-kk/vendor.xml
		and place it in ~/Android/.repo/local_manifest.xml (or ~/'name you chose'/.repo)

Then to sync up:

    repo sync
