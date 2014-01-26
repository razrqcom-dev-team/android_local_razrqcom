android_local_razrqcom
======================

Local Manifest for AOSP/CAF KitKat on Motorola msm8226 devices

Getting Started
---------------

To get started with Android, you'll need to get
familiar with [Git and Repo](http://source.android.com/download/using-repo).

Make a build directory:

	mkdir Andoid (or substitute whatever name you choose - refered to as Android from here on)
	cd Android
	mkdir .repo/local_manifests

To initialize your local repository using the Code Aurora manifest, use commands like these:

    repo init -u git://codeaurora.org/platform/manifest.git -b release -m default_LNX.LA.3.5-08410-8x26.0.xml

    curl -L -o .repo/local_manifests/aosp-caf-8226.xml -O -L https://raw.github.com/razrqcom-dev-team/android_local_razrqcom/aosp-caf-8226/aosp-caf-8226.xml
 
        ( or Download: https://github.com/razrqcom-dev-team/android_local_razrqcom/blob/aosp-caf-8226/aosp-caf-8226..xml
		and place it in ~/Android/.repo/local_manifest.xml (or ~/'name you chose'/.repo)

You will need to patch InCallUi, system/core and device/qcom/msm8226, use commands like these:

    cd ~/Android/system/core
    wget https://raw2.github.com/razrqcom-dev-team/android_local_razrqcom/aosp-caf-8226/caf_8226_system_core.patch
    git am --signoff < caf_8226_system_core.patch
    cd ~/Android/device/qcom/msm8226
    wget https://raw2.github.com/razrqcom-dev-team/android_local_razrqcom/aosp-caf-8226/caf_8226_device.patch
    git am --signoff < caf_8226_device.patch
    cd ~/Android/packages/apps/InCallUi
    wget https://raw2.github.com/razrqcom-dev-team/android_local_razrqcom/aosp-caf-8226/caf_8226_InCallUi.patch
    git am --signoff < caf_8226_InCallUi.patch

Then to sync up:

    repo sync
