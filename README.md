[Emotion Rom](http://emotroid.com/)
====================================

![Emotroid Team](http://i.imgur.com/4XAXvMq.png)

Download the Source
===================

Please read the [AOSP building instructions](http://source.android.com/source/index.html) before proceeding.

Initializing Repository
-----------------------

Initiate core trees without any device/kernel/vendor:

    $ repo init -u https://github.com/EmotionV20/platform_manifest.git -b nougat
    
After collect roomservices:

    $ cd .repo
    $ git clone https://github.com/EmotionV20/local_manifests.git
    $ cd back to working directory

Sync the repository:

    $ repo sync -c -f -j4 --force-sync --no-clone-bundle

***

Building
--------

After the sync is finished, please read the [instructions from the Android site](http://s.android.com/source/building.html) on how to build.

    $ ./build-emotion.sh <device_codename>

Example for v20:

    $ ./build-emotion.sh ls997

For a list of supported options, run the script on it's own:

    $ ./build-emotion.sh


Remember to `make clobber && make clean` every now and then!
