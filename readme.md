# Download Private Vimeo video.
## Requirements
* Download and python installer (3.11.6 version) from https://www.python.org/downloads/
* Download this repository code: use "git clone" or click on "Code" button and select "Download Zip" option and decompress contents.
* Download ffmpeg zip ffmpeg-master-latest-win64-gpl.zip
 from https://github.com/BtbN/FFmpeg-Builds/releases and copy the ffmpeg.exe file in the same folder you decompressed the previous Zip (git repository).
* Open cmd.exe and go to that folder.
* Execute ´pip -r requirements.txt`
## Download Vimeo file
* Open your video on your browser (e.g. Chrome) and open the development tools window (Chrome: CTRL+MAY+I).
* Go to "Network" tab, play the video and search for some entry like this: "master.json?base64_init=1&query_string_ranges=1"
* Copy the complete URL (e.g. https://55vod-adaptive.akamaized.net/.../master.json?base64_init=1&query_string_ranges=1) and remove the end of the string "&query_string_ranges=1" (so you get something like this: https://55vod-adaptive.akamaized.net/.../master.json?base64_init=1)
* Open cmd.exe and go to the script folder.
* Execute python main.py --url https://55vod-adaptive.akamaized.net/.../master.json?base64_init=1 --output result-video-filename
* The result file should be stored in output directory