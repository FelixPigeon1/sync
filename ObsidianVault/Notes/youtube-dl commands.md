
!L0v3H@t$un3M!ku - twitch p

youtube-dl -x --audio-format mp3 -a C:\Windows\list.txt -o C:\Users\share\Music\%(playlist_index)s-%(title)s.%(ext)s

youtube-dl -x --audio-format mp3 -a C:\Windows\list.txt -o C:\Users\share\Music\%(title)s.%(ext)s


Silly little text document for downloading songs!
Lines that start with a '#' will not be read by the program

https://github.com/ytdl-org/youtube-dl - refer to here if you need to look something up

You will have to change the file paths for where to A: find this text document and B: save your downloads

--Downloads videos in a playlist and numbers them, saves as audio only--
youtube-dl -x -R 20 --rm-cache-dir --audio-format mp3 --add-metadata -a C:\Windows\list.txt -o C:\Users\share\Music\%(album)s\%(playlist_index)s-%(title)s.%(ext)s
         audio only                                                       text file path            save file path       all the '%' shits are format codes for python the github page has a list of all the ones that you can use 
--Downloads a single video as audio only--
youtube-dl -x -R 20 --rm-cache-dir --audio-format mp3 --add-metadata -a C:\Windows\list.txt -o C:\Users\share\Music\%(album)s\%(title)s.%(ext)s
https://www.youtube.com/watch?v=7E0fVfectDo&list=OLAK5uy_mlKh6oTkQAOx2YUy-XFGhkfb_rw4lJQJw
