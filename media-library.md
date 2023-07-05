# Media Library

I wanted to build my own local storage for digital media that I have purchased, such as movies and TV shows. I did have this idea for a long time, but I did not know even where to begin. I got motivated by [Jeff Geerling's video](https://youtu.be/RZ8ijmy3qPo) and [blog post](https://www.jeffgeerling.com/blog/2022/streaming-services-lost-plot) on unsubscribing from various streaming services and building one's own collection. Furthermore, I did not have too much information about this beforehand, so I built this blog post to help any other beginners out there who are interested in building their own local collection. Of course, you can "sail the high seas", but I will not be discussing any of that here.

## Pricing

Personally, price is really important for me when I think about pursuing a project or think about investing in a subscription. That is why I will be creating a chart which reflects how much ideally I would be paying for these services. Here is how much streaming services are currently charging (as of March 2023) for the bundle that has HD (1080p) content in it:

| Name        | Price (Monthly in USD) | Plan                       |
| ----------- | ---------------------- | -------------------------- |
| Netflix     | 15.49                  | 2 devices at once, Ad-free |
| Hulu        | 7.99                   | Ad-supported content       |
| Prime Video | 8.99                   | Ad-free                    |
| Disney Plus | 7.99                   | Ad-supported content       |
| HBO Max     | 9.99                   | Ad-supported content       |
| Crunchyroll | 7.99                   | Ad-free                    |

In order to watch the shows you want to watch, you end up paying a good amount. Plus, these companies have proven time and time again, that they will drop and pick up any shows that they want. This is where building your own library comes into play. **You** get to choose what you want in the library. In addition, you can get the raw quality of the movie (ex. 4k movies). Here is the pricing for the hardware and software I paid for in order to build my own video media library:

| Name                                                                           | Type                            | Price (USD)                     |
| ------------------------------------------------------------------------------ | ------------------------------- | ------------------------------- |
| LG Electronics Ultra Slim Portable Blu-ray/DVD Writer Optical Drive - BP60NB10 | Optical Drive                   | 109.99                          |
| WD 6TB My Book Desktop External Hard Drive - WDBBGB0060HBK-NESN                | Hard Drive                      | $97.75                          |
| MakeMKV                                                                        | Transcoder (Converter) Software | 60                              |
| Movies and Shows purchased in hard copy (DVD/Blu-ray)                          | Media                           | Depends on your content library |

If you want to see the size of the output file before buying a DVD or Blu-ray Disk, I would recommend checking out [https://thediscdb.com/](https://thediscdb.com/) or asking in the MakeMKV Forum or subreddit.

There are some movies that are native 4K and some are upscaled to that resolution. I use the following to check what the native resolution of a movie/show is: [https://www.blu-ray.com/](https://www.blu-ray.com/) and [https://thedigitalbits.com/columns/the-4k-uhd-release-list/4k-uhd-list-01](https://thedigitalbits.com/columns/the-4k-uhd-release-list/4k-uhd-list-01). You can also search online for "(movie name) tech specs" and see what is stated for "Digital Intermediate". If it says 2K for the intermediate, then it is upscaled. If it says 4K for the Intermediate, then it is native.

## Video Conversion

### Video Encoding 101

Video encoding is the process of converting RAW video into an output. Digital videos need to be encoded in order to be played on various platforms, as some cannot handle RAW data. Video encoding is sometimes referred to as video compression, and decoding is referred to as decompression. Video encoding involves two main processes: compression and transcoding. Compression significantly decreases the size of the video file, so it is more manageable. This allows the file to be able to load quickly or be uploaded much faster online (because the file is smaller). Transcoding refers to the audio and video conversion from one format to another. It ensures that a video file is compatible with the video player and/or platform it is using. Without transcoding, users would not be able to watch the video file at all.

### Codecs 101

A codec is a method for compressing or decompressing data (in this case, a video file) so it can be easily transported to different applications. Choosing the right codec can result in the desired quality, file size, or encode speed. Here are some examples of Codecs: x264, x265, FFmpeg, DivX, and Xvid.

### Containers 101

A container combines an encoded audio stream (audio codec), encoded video stream (video codec), and metadata in a single video file. Each container supports a different range of video codecs. Examples of video containers are MP4, MKV, AVI, WMA, MOV, FLV, etc. Usually, you will see these as extensions to video files (ex. Movie.mp4).

### Video Resolutions

This is just a chart I wanted to put in here just for comparison of the various resolutions for video.

| Resolution Type            | Common Name | Aspect Ratio | Pixel Size  |
| -------------------------- | ----------- | ------------ | ----------- |
| SD (Standard Definition)   | 480p        | 4:3          | 640 x 480   |
| HD (High Definition)       | 720p        | 16:9         | 1280 x 720  |
| Full HD (FHD)              | 1080p       | 16:9         | 1920 x 1080 |
| QHD (Quad HD)              | 1440p       | 16:9         | 2560 x 1440 |
| 2K video                   | 1080p       | 1:1.77       | 2048 x 1080 |
| 4K video or Ultra HD (UHD) | 4K or 2160p | 1:1.9        | 3840 x 2160 |
| 8K video or Full Ultra HD  | 8K or 4320p | 16∶9         | 7680 x 4320 |

### DVD vs. Blu-ray

I never knew the difference between DVD and Blu-ray, other than the name. I made this chart to make it clearer for others in the same position as myself.

|                                  | DVD                                                        | Blu-ray                                                                                                                                                       |
| -------------------------------- | ---------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Media type                       | Optical disc                                               | High-density optical disc                                                                                                                                     |
| Storage Capacity                 | <p>4.7GB (single-layer)<br>8.5GB (dual-layer)</p>          | <p>25GB (single-layer)<br>50GB (dual-layer)</p>                                                                                                               |
| Laser wavelength                 | 650nm (red laser)                                          | 405nm (blue laser)                                                                                                                                            |
| Hard coating                     | No                                                         | Yes                                                                                                                                                           |
| Data transfer rate (video/audio) | 10.08 Mbps                                                 | 54.0 Mbps                                                                                                                                                     |
| Max video resolution             | 480p,576p                                                  | <p>1080p<br>2160p<br>4k Ultra HD</p>                                                                                                                          |
| Video codecs                     | MPEG-2                                                     | <p>MPEG-2<br>MPEG-4 AVC<br>SMPTE VC-1</p>                                                                                                                     |
| Audio codecs                     | <p>Linear PCM<br>Dolby Digital<br>DTS Digital Surround</p> | <p>Linear PCM<br>Dolby Digital<br>Dolby Digital Plus<br>Dolby TrueHD<br>DTS Digital Surround<br>DTS-HD</p>                                                    |
| Usage                            | <p>Animations<br>Movies<br>Videos</p>                      | <p>Data storage<br>High-definition video (1080p) High-definition audio<br>Stereoscopic 3D<br>PlayStation 3 games<br>PlayStation 4 games<br>Xbox One games</p> |
| Content protection system        | CSS 40-bit                                                 | AACS-128bit / BD+                                                                                                                                             |

### H.264 vs. H.265

H.264 and H.264 are popular codecs used to encode video media. I did not know the difference between them as well, so I looked online to see what I could find. Here are some of the differences between them:

|                                          | H.264                                                                     | H.265                                                                        |
| ---------------------------------------- | ------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| Known as                                 | AVC (Advanced Video Coding)                                               | HEVC (High Efficiency Video Coding)                                          |
| Supported container formats              | mkv, mp4, qtff, asf, avi, mxf, ps, ts, m2ts, evo, 3gp, f4v                | mkv, mp4, qtff, asf, avi, mxf, ps, ts, 3gp                                   |
| Recommended bandwidth for video encoding | <p>480p — 1.5 Mbps<br>720p — 3 mpbs<br>1080p — 6 Mbps<br>4K — 32 mbps</p> | <p>480p — 0.75 Mbps<br>720p — 1.5 mpbs<br>1080p — 4 Mbps<br>4K — 15 mbps</p> |

H.264 seems to be used as there is a lot more compatibility with it. However, there is a growth in the use of the H.265 due to it having a smaller footprint, and it is more efficient, thus allowing it to be good for streaming services.

## Drive Testing

In order to make sure that the drives you have are internally "good", there are checks you can do to make sure of that. You can kind of think of this as stress testing the system to make sure it is able to function as expected. There are a lot of good recommendations on r/DataHoarder at [https://www.reddit.com/r/DataHoarder/wiki/index/#wiki\_possible\_pages.2Farticles\_for\_wiki](https://www.reddit.com/r/DataHoarder/wiki/index/#wiki\_possible\_pages.2Farticles\_for\_wiki) (Check 5.3.1-5.3.4). From my research, they essentially break down to the following tests (some are for Linux and others for Windows):

| Test               | Command(s)                                                                                                                                                                                         | Note                                                                                                        |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| SMART long test    | <p>smartctl -A /dev/sdxx<br>smartctl -t long /dev/sdxx</p>                                                                                                                                         | Device has to be SMART compatible                                                                           |
| SMART short test   | smartctl -t short /dev/sdxx                                                                                                                                                                        | Device has to be SMART compatible                                                                           |
| badblocks          | badblocks -wsv -b 4096 -t 0x55 -o \~/output\_file.txt /dev/sdxx                                                                                                                                    | badblocks is a Linux utility to check for bad sectors on a disk drive.                                      |
| fio                | sudo fio --filename=/dev/sdxx --name=randwrite --ioengine=sync --iodepth=1 --rw=randrw --rwmixread=50 --rwmixwrite=50 --bs=4k --direct=0 --numjobs=8 --size=300G --runtime=7200 --group\_reporting | fio spawns a number of threads or processes doing a particular type of I/O action as specified by the user. |
| h2testw            | Has GUI, read more: https://3ds.hacks.guide/h2testw-(windows).html                                                                                                                                 |                                                                                                             |
| Hard Disk Sentinel | Has GUI, read more: https://www.hdsentinel.com/                                                                                                                                                    |                                                                                                             |

I would also recommend checking out [https://github.com/Spearfoot/disk-burnin-and-testing](https://github.com/Spearfoot/disk-burnin-and-testing) for those who use Linux. **Do your own research on these before using them.** I have seen people use SMART tests for health checking drives, and the rest of the software for actually stress testing the drive. Everybody has a different preference for how much to stress test their systems. I myself used the following command `sudo badblocks -wsv -b 4096 -t 0x55 -o output.txt /dev/sdxx`, and it took 23 hours 54 minutes and 51 seconds to complete for a 6 TB hard drive. After this, I encrypted the drive.

## MakeMKV (Windows)

In order to set up MakeMKV, there is some setup you have to do to get it to work. **Do your own security due diligence for anything listed here. This is what worked for me.** Here is the list:

* [ ] Download Java Runtime Engine. See [https://www.makemkv.com/bdjava/](https://www.makemkv.com/bdjava/) for more info.
* [ ] Download MakeMKV from [https://makemkv.com/download/](https://makemkv.com/download/)
* [ ] Purchase a key ($60) or grab the free beta key (lasts one month) from [https://forum.makemkv.com/forum/viewtopic.php?f=5\&t=1053](https://forum.makemkv.com/forum/viewtopic.php?f=5\&t=1053)
* [ ] Download the SDFtool Flasher from [https://forum.makemkv.com/forum/viewtopic.php?f=16\&t=22896](https://forum.makemkv.com/forum/viewtopic.php?f=16\&t=22896)
* [ ] Download the "All You Need Firmware Pack" from [https://forum.makemkv.com/forum/viewtopic.php?f=16\&t=22896](https://forum.makemkv.com/forum/viewtopic.php?f=16\&t=22896) as well

### Steps

1. Connect the Optical Disk to your PC.
2. Open the MakeMKV software (I have covered my Serial Number for my device)

<figure><img src=".gitbook/assets/1a50e41dc7fd4bfa8b2d0679e976d13c.cleaned.png" alt=""><figcaption></figcaption></figure>

3. Use the SDFtool Flasher and the respective bin file to flash the optical drive.
   1. I used the GUI, so I did not have to deal with the command line for this
   2. The bin file will have the optical drive name in the file name (ex. DE\_LG\_**BP60NB10**-NB12\_1.02-MK.bin)

<figure><img src=".gitbook/assets/27637c7a45dd45c799b2e8ea856c004e.cleaned.png" alt=""><figcaption></figcaption></figure>

4. The Information should look different (if done correctly)

<figure><img src=".gitbook/assets/2b4cb44738a448d380d3a71a09040200.cleaned.png" alt=""><figcaption></figcaption></figure>

5. Insert the DVD/Blu-ray disc into the optical drive
   1. Can be done manually by pressing the button on the drive **or** by clicking the "eject" button on the toolbar
   2. The "Data capacity" field lets you know the size of the output file (although I have covered it, just for covering my own ass)

<figure><img src=".gitbook/assets/965b4693304447979ebf5e348440d901.cleaned.png" alt=""><figcaption></figcaption></figure>

6. Click on the optical drive icon

<figure><img src=".gitbook/assets/ca43c570f0b943cbb96d1aad02b56ea8.cleaned.png" alt=""><figcaption></figcaption></figure>

7. Select the files you want and choose an output folder. Then click on the icon under "Make MKV"

<figure><img src=".gitbook/assets/06d235bbdf5e4154a6572053d1800754.cleaned.png" alt=""><figcaption></figcaption></figure>

8. Wait for the process to complete

### Helpful MakeMKV links

1. UHD F.A.Q.: [https://forum.makemkv.com/forum/viewtopic.php?f=12\&t=16883](https://forum.makemkv.com/forum/viewtopic.php?f=12\&t=16883)
2. Is my movie native 4k or upscaled 4k?: [Google Spreadsheet Link](https://docs.google.com/spreadsheets/d/1XgBqUDMwN-\_CvbQssa7KVY\_j56kimrgfePAH7i3dStM/edit)

## Post MakeMKV

I was only after the "Raw" output from MakeMKV. However, there are more pathways you can go from here. Here are a couple that I have seen others do.

### Playback

Here are some of the media players that I have used to watch digital content: **mpv.io** and **VLC**. I have seen mpv.io be recommended time and time again in various channels relating to media storage. I have also heard about MPC-HC be good for MakeMKV output as well.

### Handbrake

Handbrake is a video transcoding tool that allows you to covert video to other codecs. This allows you to decrease the size of the file exponentially, while maintaining a good amount of the quality. I have heard people decrease the size of videos by 3-5x using transcoding. There are a lot of presets that handbrake has, which one can use for easy transcoding. I have seen others have their own presets and own methods, which they have worked on over their tenure using Handbrake. In Jeff's video, he uses the **HQ 1080p30 Surround** preset. For 4k videos, he goes to the "Dimensions" tab, and changes the "Resolution Limit" from **1080p HD** to **2160p 4k Ultra HD**. I did try to use Handbrake, just to play around with it. It ended up using ALL of my GPU resources. Here are some tips I found (not tested) that have seemed to work for others:

In Handbrake (Windows/Linux):

* Set "Video" > "Advanced Options" to: -x threads=1
* Set "Video" > "Advanced Options" to: --encoder-preset=veryslow
* (combination) Set "Video" > "Advanced Options" to: --encoder-preset=veryslow -x threads=1
* Set "Video" > "Advanced Options" to: pools=<**enter number here**>
  * This ends up working for most people

In Windows:

* Open the "Task Manager" application
* Click on the "Details" tab and scroll to Handbrake (Handbrake.exe)
* Right Click on it and select "Set Affinity"
* Enable or disable any CPU cores you want

In Windows (as well):

* Open Handbrake > Tools > Preferences
* Go to the "Advanced" tab and find "Priority Level"
* From the dropdown, choose "Below Normal" or "Low"
  * Handbrake will be given less CPU when other tasks are being done

### NAS

A network attached storage (NAS) is a way to have multiple people on the network be able to access shared resources. There are many companies that are notable in the NAS community: QNAP, Synology, and ASUSTOR. Just a FYI, this can get expensive really fast. With a NAS, you can store your video files in one location, and anybody on the network can access it. This is great for family uses, since any member can view what they want, without "bothering" others. Using something like [Jellyfin](https://jellyfin.org/) can make this have a great web user interface for you and others to use.

## Stats

As this is an educational blog, here are some stats for media I was able to convert.

| Type                  | Duration   | File Size |
| --------------------- | ---------- | --------- |
| Movie (4K - Upscaled) | 1H:43M:27S | 58.4 GB   |
|                       |            |           |

## Sources

* [https://www.rapidseedbox.com/blog/guide-to-mastering-handbrake](https://www.rapidseedbox.com/blog/guide-to-mastering-handbrake)
* [https://www.cloudflare.com/learning/video/video-encoding-formats/](https://www.cloudflare.com/learning/video/video-encoding-formats/)
* [https://typito.com/blog/video-resolutions/](https://typito.com/blog/video-resolutions/)
* [https://www.reddit.com/r/DataHoarder/comments/7wh4a6/comment/du2elge/](https://www.reddit.com/r/DataHoarder/comments/7wh4a6/comment/du2elge/)
* [https://www.diffen.com/difference/Blu-ray\_vs\_DVD](https://www.diffen.com/difference/Blu-ray\_vs\_DVD)
* [https://www.samsung.com/in/support/tv-audio-video/what-is-the-difference-between-blu-ray-disc-dvd-and-cd/](https://www.samsung.com/in/support/tv-audio-video/what-is-the-difference-between-blu-ray-disc-dvd-and-cd/)
* [https://www.vidmore.com/knowledge/blu-ray-vs-dvd/](https://www.vidmore.com/knowledge/blu-ray-vs-dvd/)
* [https://www.macxdvd.com/mac-dvd-video-converter-how-to/x264-vs-x265.htm](https://www.macxdvd.com/mac-dvd-video-converter-how-to/x264-vs-x265.htm)
* [https://www.tomshardware.com/reference/h264-h265-hevc-codec-definition](https://www.tomshardware.com/reference/h264-h265-hevc-codec-definition)
* [https://www.brid.tv/h264-vs-h265/](https://www.brid.tv/h264-vs-h265/)
* [https://www.macxdvd.com/mac-dvd-video-converter-how-to/handbrake-high-cpu-usage.htm](https://www.macxdvd.com/mac-dvd-video-converter-how-to/handbrake-high-cpu-usage.htm)
* [https://www.reddit.com/r/4kbluray/comments/10zd22d/is\_there\_a\_way\_to\_know\_whether\_a\_4k\_bluray\_is/](https://www.reddit.com/r/4kbluray/comments/10zd22d/is\_there\_a\_way\_to\_know\_whether\_a\_4k\_bluray\_is/)
