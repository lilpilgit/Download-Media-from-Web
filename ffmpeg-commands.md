## FFMPEG useful tips&tricks

# Download a video from a M3U8 file
Using Chrome/Firefox web developer tool, find during buffering of streamed film, the server that host index M3U8, and launch this command:

```console
foo@bar:~$ ffmpeg -protocol_whitelist file,http,https,tcp,tls,crypto -i https://host.example.com/path_m3u8_index_file -c copy OUTPUT_FILM_NAME.ts
foo@bar:~$ ffmpeg -i OUTPUT_FILM_NAME.ts -map 0 -c copy OUTPUT_FILM_NAME.mkv
```
