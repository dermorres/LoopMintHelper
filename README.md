# LoopMintHelper
This is a little bash Script that is able to semi-automate and fasten up the process of minting NFTs on Looprings Layer 2!

In fact it can do the following:
1. batch rename mediafiles (you have a collection of mediafiles that can be renamed to collectionname0000 (the zeroes are variable in count)
2. upload mediafiles to ipfs and remote pin them to a remote pinning service
3. construct mass metadata for a collection (no matter if one nft or 10.000!)
4. upload and pin these too
5. hand the CIDs of the metadata over to Fudgebuckets LoopMintSharp, to automatically mint all of them.

It can not yet(but soon):
1.handle traits
2.do individual amounts per nft if you mint them all together
3.do individual descriptions per nft (names and numbers will already be dynamic per nft)

Yo can skip every step of it and enter at a later point! And you can also upload the files yourself and just ender the asked CID in the script!

With this, you can save all the time it would take to upload, copy cids and pinning files, as well as the tedious editing of metafiles.
At this time, the script cannot insert traits, but that will come soon!



## Prerequisites and installation (looks like more than it is!)
At the moment a running linux system, windows support may come soon!

1.Install IPFS Desktop (if you want to use remote pinning service! if not, only the cli is enough!)
->https://docs.ipfs.io/install/ipfs-desktop/#ubuntu
2.when you downloaded it, start it and go into the settings (left side) and activate a Remote Pinning Service here (atm mandatory to use the pinning feature!)

3.Download FudgeBuckets phenomenal LoopMintSharp (which latently inspired me to do this)
->https://github.com/fudgebucket27/LoopMintSharp/releases/download/Linux_x64_v2/linux-x64.zip

4.Download my script here and extract the content of the zip into an own folder somewhere you like.

5.Extract from Fudgebuckets LoopMintSharp only the file also called LoopMintSharp into the directory you extracted my files into! DO NOT copy the appsettings.json from Fudgebucket, as a slightly modificated version (only two placeholders which let me edit it with the script, so you get the right nft amount and royaltypercentage) already came with my script.

6.Open the "appsettings-base.json" file and enter into the first 4 fields (the empty "" before the //comments) appropriately like the comments on the right tell you. you can find the data you need to fill in on loopring.io or in your mobile wallet!

7.EITHER open a terminal in the folder of the script and type "chmod +x LoopMintSharp" 
OR right click on LoopMintSharp->Setting->Permissions->check "Allow executing file as program"
do the exact same for "loopminthelper.sh"!

ALL DONE! 


You can use the script now by either double clicking on it and run it,
or you run a terminal in the folder of the script and type "./loopminthelper.sh"


## TIPPS:
1.Do not panic if it seems like frozen for a few seconds, it is most likely an intentional background check if you are copying mediafiles into the folder!
2.Read everything that pops up! 
3.Type carefully, as a mistake may for example need you to restart the process, as the mstake would be in every metafile.



If you encounter any problems, please feel free to reach out!
Reddit: dermorres
Discord: https://discord.gg/NwfJCd7bah
