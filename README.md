# ULTIMIATE-GUIDE-IRL-STREAM-BELABOX-GOPRO
This is a How-To for the IRL streaming setup with a GoPro(Hero 11 Black) (and the belabox). I found it really difficult to get all the information needed to set up a stream using a GoPro. There were SO many sites I had to visit to make it work. This guide shall help you overcome these hurdles to make life easier for upcoming streamers! The coming sections describe a setp-by-step guide, starting from a simple setup with only a GoPro and your phone. The next sections will require more equipment to make streaming work more seamlessly!
1) How to stream from the GoPro to twitch using mobile phone. 
2) How to setup RTMP server at home and stream using OBS.
3) How to stream with the belabox.

During the writing of this guide I was using the GoPro Quick app version: 11.18.1(15524)!
I was also using an android phone (Samsung Galaxy S20+) with Android 13. For some steps you will have to look up on how to do them on Iphone (sorry about that!)

## 1. Streaming from the GoPro to twitch.tv
0) OPTIONAL: Create a GoPro account (gopro.com). This just helps, so you do not have to click "Continue as guest" every time you open the app. Trust me, it WILL get annoying at some point.
1) Install GoPro Quik app on your phone. Optional: Login with your account created in step 0) (click on the "person icon" on the top left)
2) Click on the "GoPro" icon on the bottom bar (there should be four icons: Mural, Media, Studio, GoPro)
3) Connect your GoPro with your phone
   1. on your GoPro: swipe down, swipe left, click on Preferences, Wireless Connections, Connect Device, GoPro Quick App
      Follow the steps described.
   2. After successful connection you should see a layout where you can control your GoPro. On the upper side you should see fields with "Live Stream", "View Media", "Auto Upload". Click on "Live Stream".
   3. Click on whatever platform you want to stream on. In this guide we will take TWITCH
   4. Next step depends on what network you want to use:
      1. Mobile Hotspot: Go to the settings of your phone and activate Mobile Hotspot (Android: Settings->Connections->Mobile Hotspot and     
         Tethering: activate Mobile Hotspot (you can configure it with your own password etc., not going into detail here)
      2. select that network in the GoPro app. IF for some reason the connection will not come up just restart the app. Make sure you close
          it also when it's active in the background!
      3. Choose a title for your stream. BEWARE that you can only use 150 characters for the title. The GoPro app will not show how many 
           characters you used for the title. I suggest you type it in a notepad on your phone before and save it. That way you can always                retrieve when your connection should break up and you have to restart your stream again! Trust me, this is going to happen A LOT! ;)
      4. choose resolution (depending on your network, Lens, if you want to save the VOD or not
      5. click on continue when it is highlighted (after you have chosen your network and a title!)
      6. wait a little bit on the next screen, this can take a little bit (around 1-2 minutes max!), click on "Go Live".

WELL DONE! You have successfully started your stream from the GoPro directly to twitch! :) But from here your actual journey begins!
I do not recommend using this approach as your main go-to for streaming, since you will have a lot of disconnections and your stream will just stop. You will end up with a lot of cut VOD (10 second VOD, 32 seconds, 2 hours...) It will always depend on the mobile network how your stream will go!
So if you want a more reliable stream, go ahead and read section 2! Here you will not end up losing your viewers due to disconnects! :)

## 2. Creating your own RTMP server on your Home PC
This part will describe on how you set up your local RTMP server and streaming from the GoPro directly to that server! Also I will describe how you set up your OBS so you can stream that feed to twitch. As I said in section 1, this is a more reliable approach, since the stream will not end when your mobile connection drops.
NOTE: This part is done on WINDOWS 11! (Section 3 will show how to get the SRTLA relay server going on Ubuntu 22!) 

1. Download the Monaserver files here: https://www.toolsforgopro.com/dl/monaserver.zip
2. Open the Monaserver.ini file and scroll down to [RTMP]
3. Change host to your local IP (ipconfig->ipv4 address) Lots of guides for this on the internet
4. Choose a port e.g. 1935
5. Choose same publicPort
6. write your WAN IP in publicHost (search whatismyip on google)
7. Save the file and close it
8. In the Monaserver folder, go into the "www/live" folder (if live does not exist, create it), create a folder with your STREAM-KEY (needed later for the address stream with the gopro
   -> it should look like this now: Monaserver/www/live/YOURSTREAMKEY
9. 
