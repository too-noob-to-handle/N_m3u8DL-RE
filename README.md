#N_m3u8DL-RE
Cross-platform DASH/HLS/MSS download tool. Support on-demand and live streaming (DASH/HLS).

[![img](https://img.shields.io/github/stars/nilaoda/N_m3u8DL-RE?label=%E7%82%B9%E8%B5%9E)](https://github.com /nilaoda/N_m3u8DL-RE) [![img](https://img.shields.io/github/last-commit/nilaoda/N_m3u8DL-RE?label=%E6%9C%80%E8%BF%91% E6%8F%90%E4%BA%A4)](https://github.com/nilaoda/N_m3u8DL-RE) [![img](https://img.shields.io/github/release/nilaoda/ N_m3u8DL-RE?label=%E6%9C%80%E6%96%B0%E7%89%88%E6%9C%AC)](https://github.com/nilaoda/N_m3u8DL-RE/releases) [ ![img](https://img.shields.io/github/license/nilaoda/N_m3u8DL-RE?label=%E8%AE%B8%E5%8F%AF%E8%AF%81)](https: //github.com/nilaoda/N_m3u8DL-RE) [![img](https://img.shields.io/github/downloads/nilaoda/N_m3u8DL-RE/total?label=%E4%B8%8B%E8 %BD%BD%E9%87%8F)](https://github.com/nilaoda/N_m3u8DL-RE/releases)



---

The terminal that comes with a lower version of the Windows system may not support this program. Alternative: run it in [cmder](https://github.com/cmderdev/cmder).

Arch Linux is available from the AUR: [n-m3u8dl-re-bin](https://aur.archlinux.org/packages/n-m3u8dl-re-bin), [n-m3u8dl-re-git](https: https://aur.archlinux.org/packages/n-m3u8dl-re-git)

```bash
# Arch Linux and its derivatives install the N_m3u8DL-RE distribution
yay -Syu n-m3u8dl-re-bin

# Arch Linux and its derivatives install N_m3u8DL-RE development version
yay -Syu n-m3u8dl-re-git
```
---

# command line arguments
```
Description:
  N_m3u8DL-RE (Beta version) 20230628

Usage:
  N_m3u8DL-RE <input> [options]

Arguments:
  <input>  链接或文件

Options:
   --tmp-dir <tmp-dir> set temporary file storage directory
   --save-dir <save-dir> set output directory
   --save-name <save-name> set save file name
   --base-url <base-url> set BaseURL
   --thread-count <number> Set the number of download threads [default: 16]
   --download-retry-count <number> Number of retries for each segment download error [default: 3]
   --auto-select automatically select the best track of all types [default: False]
   --skip-merge skip merging shards [default: False]
   --skip-download skip download [default: False]
   --check-segments-count Check whether the actual number of downloaded segments matches the expected number [default: True]
   --binary-merge binary merge [default: False]
   --del-after-done delete temporary files after done [default: True]
   --no-date-info Do not write date info when muxing [default: False]
   --no-log turn off log file output [default: False]
   --write-meta-json Whether to output the parsed information to a json file [default: True]
   --append-url-params Add the Params of the input Url to the fragment, useful for some websites, such as kakao.com [default: False]
   -mt, --concurrent-download download selected audio, video and subtitles concurrently [default: False]
   -H, --header <header> Set specific request headers for HTTP requests, for example:
                                            -H "Cookie: mycookie" -H "User-Agent: iOS"
   --sub-only select subtitle track only [default: False]
   --sub-format <SRT|VTT> Subtitle output type [default: SRT]
   --auto-subtitle-fix automatically fix subtitles [default: True]
   --ffmpeg-binary-path <PATH> Full path of ffmpeg executable program, for example C:\Tools\ffmpeg.exe
   --log-level <DEBUG|ERROR|INFO|OFF|WARN> set log level [default: INFO]
   --ui-language <en-US|zh-CN|zh-TW> set UI language
   --urlprocessor-args <urlprocessor-args> This string will be passed directly to the URL Processor
   --key <key> Set the decryption key, the program calls mp4decrpyt/shaka-packager to decrypt. Format:
                                            --key KID1:KEY1 --key KID2:KEY2
   --key-text-file <key-text-file> Set the key file, the program will search for the KEY by KID from the file to decrypt. (It is not recommended to use very large files)
   --decryption-binary-path <PATH> The full path of the tool used for MP4 decryption, for example C:\Tools\mp4decrypt.exe
   --use-shaka-packager Use shaka-packager instead of mp4decrypt when decrypting [default: False]
   --mp4-real-time-decryption Decrypt MP4 fragments in real time [default: False]
   -M, --mux-after-done <OPTIONS> Attempt to mux separated video and audio when all work is done. Type "--morehelp mux-after-done" for details
   --custom-hls-method <METHOD> Specify HLS encryption method (AES_128|AES_128_ECB|CENC|CHACHA20|NONE|SAMPLE_AES|SAMPLE_AES_CTR|UNKNOWN)
   --custom-hls-key <FILE|HEX|BASE64> Specify HLS decryption KEY. Can be file, HEX or Base64
   --custom-hls-iv <FILE|HEX|BASE64> Specify HLS decryption IV. Can be file, HEX or Base64
   --use-system-proxy use system default proxy [default: True]
   --custom-proxy <URL> set request proxy, such as http://127.0.0.1:8888
   --custom-range <RANGE> Only download some shards. Type "--morehelp custom-range" to see details
   --task-start-at <yyyyMMddHHmmss> Do not start tasks before this time
   --live-perform-as-vod download live stream on demand [default: False]
   --live-real-time-merge Real-time merge when recording live [default: False]
   --live-keep-segments Keep segments when recording live and enable live merge [default: True]
   --live-pipe-mux When recording live broadcast and enabling real-time merging, real-time mixing to TS files via pipeline + ffmpeg [default: False]
   --live-fix-vtt-by-audio fix VTT subtitle by reading start time of audio file [default: False]
   --live-record-limit <HH:mm:ss> Recording time limit when recording live
   --live-wait-time <SEC> Manually set the live list refresh interval
   --mux-import <OPTIONS> Import external media files when muxing. Type "--morehelp mux-import" for details
   -sv, --select-video <OPTIONS> Select video streams that meet the requirements by regular expressions. Type "--morehelp select-video" to see details
   -sa, --select-audio <OPTIONS> Select audio streams by regular expression. Type "--morehelp select-audio" for details
   -ss, --select-subtitle <OPTIONS> Select subtitle streams that meet the requirements through regular expressions. Type "--morehelp select-subtitle" to see details
   -dv, --drop-video <OPTIONS> Drop matching video streams by regular expression.
   -da, --drop-audio <OPTIONS> Remove matching audio streams by regular expression.
   -ds, --drop-subtitle <OPTIONS> Remove matching subtitle streams by regular expression.
   --morehelp <OPTION> View detailed help information for an option
   --version Show version information
   -?, -h, --help Show help and usage information
```

<details>
<summary>Click to view More Help</summary>

```
More Help:

 --mux-after-done

Attempts to mux separate audio and video when all work is done. You can specify the following parameters in :separated form:

* format=FORMAT: Specify the mixed stream container mkv, mp4
* muxer=MUXER: specify muxer ffmpeg, mkvmerge (default: ffmpeg)
* bin_path=PATH: Specify the program path (default: automatically search)
* skip_sub=BOOL: Whether to skip the subtitle file (default: false)
* keep=BOOL: Whether to keep the file after muxing is completed true, false (default: false)

For example:
# Mux as mp4 container
-M format=mp4
# Use mkvmerge, automatically find the program
-M format=mkv:muxer=mkvmerge
# Use mkvmerge, customize the program path
-M format=mkv:muxer=mkvmerge:bin_path="C\:\Program Files\MKVToolNix\mkvmerge.exe"
```
```
More Help:

   --mux-import

Introduce external media files when muxing. You can specify the following parameters in : delimited form:

* path=PATH: Specify the media file path
* lang=CODE: Specifies the media file language code (not required)
* name=NAME: Specifies the description information of the media file (not required)

For example:
# Import external subtitles
--mux-import path=zh-Hans.srt:lang=chi:name="Chinese (Simplified)"
# Import external audio tracks + subtitles
--mux-import path="D\:\media\atmos.m4a":lang=eng:name="English Description Audio" --mux-import path="D\:\media\eng.vtt":lang =eng:name="English (Description)"
```
```
More Help:

   --select-video

Select video streams that meet the requirements through regular expressions. You can specify the following parameters in the form of: separation:

id=REGEX:lang=REGEX:name=REGEX:codec=REGEX:res=REGEX:frame=REGEX
segsMin=number:segsMax=number:ch=REGEX:range=REGEX:url=REGEX
plistDurMin=hms:plistDurMax=hms:for=FOR

* for=FOR: selection method. best[number], worst[number], all (default: best)

For example:
# select the best video
-sv best
# Select 4K+HEVC video
-sv res="3840*":codec=hvc1:for=best
# Select videos longer than 1 hour 20 minutes 30 seconds
-sv plistDurMin="1h20m30s":for=best
```
```
More Help:

   --select-audio

Select the audio stream that meets the requirements through regular expressions. Refer to --select-video

For example:
# select all audio
-sa all
# Select the best English track
-sa lang=en:for=best
# Choose the best 2 English (or Japanese) audio tracks
-sa lang="ja|en":for=best2
```
```
More Help:

   --select-subtitle

Select subtitle streams that meet the requirements through regular expressions. Refer to --select-video

For example:
# select all subtitles
-ss all
# Select all subtitles with "Chinese"
-ss name="Chinese":for=all
```
```
More Help:

   --custom-range

When downloading on-demand content, only some segments are downloaded.

For example:
# Download [0,10] a total of 11 fragments
--custom-range 0-10
# Download subsequent fragments starting from sequence number 10
--custom-range 10-
# Download the first 100 shards
--custom-range-99
# Download the content from the 5th minute to the 20th minute
--custom-range 05:00-20:00
```

</details>




# run screenshot

## on demand

![RE1](img/RE.gif)

You can also download in parallel + automatic stream mixing


![RE2](img/RE2.gif)

## live streaming

Record TS live source:

[click to show gif](http://pan.iqiyi.com/file/paopao/W0LfmaMRvuA--uCdOpZ1cldM5JCVhMfIm7KFqr4oKCz80jLn0bBb-9PWmeCFZ-qHpAaQydQ1zk-CHYT_UbRLtw.gif)

Record MPD live source:

[click to show gif](http://pan.iqiyi.com/file/paopao/nmAV5MOh0yIyHhnxdgM_6th_p2nqrFsM4k-o3cUPwUa8Eh8QOU4uyPkLa_BlBrMa3GBnKWSk8rOaUwbsjKN14g.gif)

During the recording process, use ffmpeg to complete the real-time mixing of audio and video
```
ffmpeg -readrate 1 -i 2022-09-21_19-54-42_V.mp4 -i 2022-09-21_19-54-42_V.chi.m4a -c copy 2022-09-21_19-54-42_V.ts
```
In the new version (>=v0.1.5), you can try to open `live-pipe-mux` instead of the above command

**Special attention: If the network environment is not stable enough, please do not enable `live-pipe-mux`. ffmpeg is responsible for reading data in the pipeline, and it is easy to lose live data in some environments**

In the new version (>=v0.1.8), some options of ffmpeg in `live-pipe-mux` can be changed by setting the environment variable `RE_LIVE_PIPE_OPTIONS`: https://github.com/nilaoda/N_m3u8DL-RE/ issues/162#issuecomment-1592462532

## sponsorship

<a href="https://www.buymeacoffee.com/nilaoda" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/default-orange.png" alt="Buy Me A Coffee" height="41" width="174"></a>
