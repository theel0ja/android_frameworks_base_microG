## Android Open Source Project Frameworks Base with MicroG support

**This repo was made so anyone that wants to add MicroG support to their Rom can cherry pick from here.**

Patches source:

https://github.com/microg/android_packages_apps_GmsCore/tree/master/patches
https://github.com/microg/android_packages_apps_UnifiedNlp/tree/master/patches

__Credits to mar-v-in and others for the patches__

What each patch does:

microG-support-KK-LP.patch - Support for fake signatures for Kitkat-Lollipop

microG-support-MM.patch - Support for fake signatures for Marshmallow

microG-support-N.patch - Support for fake singatures for Nougat

microG-support-O.patch - Support for fake singatures for Oreo

microG-support-P.patch - Support for fake singatures for Pie

Location-providers.patch - Allow location providers also outside of /system

## How to apply a patch:

Download the patch file and place it into source/frameworks/base
Then use the following command for applying the patch: **patch -p1 < patchname.patch**

That should do it. Good luck. [Remeber to commit with the proper author of the commit]

## How to cherry-pick the commits required for MicroG:

Go in source/frameworks/base and run the following command:

    $ git remote add microg https://github.com/Thespartann/android_frameworks_base_microG.git

    $ git fetch microg

    $ git cherry-pick xxxx  [xxxx is the commit you want to cherry pick]

Example: [Nougat]

    $ git cherry-pick 067a593747eb28290a7a790868377613552fd988

    $ git cherry-pick 02532e93e3189a00db1f8b9f499071c14ed6695d



The Location-providers.patch patch was not cherry picked as it might be unsafe. If you still want to use it, you can apply the patch file to your frameworks base.



