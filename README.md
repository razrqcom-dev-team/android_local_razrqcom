android_local_razrqcom
======================

Local Manifest for Ubuntu Phablet on Motorola Razr Qcom devices

Getting Started
---------------

To get started with Android, you'll need to get
familiar with [Git and Repo](http://source.android.com/download/using-repo) and
https://wiki.ubuntu.com/Touch/Porting#Contributing_back

Make a build directory:

	mkdir Andoid (or whatever name you choose)
	cd Android (or the name  you chose)
	mkdir .repo/local_manifests

To initialize your local repository using the Cyanogemod manifest, use commands like these:

    phablet-dev-bootstrap [target_directory that you chose]

    curl -L -o .repo/local_manifests/phablet.xml -O -L https://raw.github.com/razrqcom-dev-team/android_local_razrqcom/phablet/phablet.xml
 
    	( or Download: https://github.com/razrqcom-dev-team/android_local_razrqcom/blob/phablet/phablet.xml
		and place it in ~/Android/.repo/local_manifest.xml (or ~/'name you chose'/.repo)

Then to sync up:

    phablet-dev-bootstrap [target_directory that you chose] -c
    On subsequent builds you may need to cd [target_directory that you chose]/ubuntu/platform-api
    and issue the command 'bzr pull' to get the latest updates.
