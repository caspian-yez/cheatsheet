yt-dlp
======

```sh
# get list of resources
yt-dlp --js-runtimes node -F URL
yt-dlp --js-runtimes node --proxy socks5://proxy.local:1080 -F URL
# get specific resource
yt-dlp --js-runtimes node -o "%(upload_date)s-[%(id)s]-%(uploader)s.%(ext)s" -f 1 URL
yt-dlp --js-runtimes node --proxy socks5://proxy.local:1080 -o "%(upload_date)s-[%(id)s]-%(uploader)s.%(ext)s" -f 1 URL
# get list info
yt-dlp --js-runtimes node --skip-download --flat-playlist --print "%(upload_date)s-[%(id)s]-%(uploader)s-%(title)s" URL
yt-dlp --js-runtimes node --proxy socks5://proxy.local:1080 --skip-download --flat-playlist --print "%(upload_date)s-[%(id)s]-%(uploader)s-%(title)s" URL
```

```sh
# get info
yt-dlp --js-runtimes node --proxy socks5://proxy.local:1080 --skip-download --flat-playlist --print "%(upload_date)s-[%(id)s]-%(uploader)s-%(title)s" URL
yt-dlp --js-runtimes node --proxy socks5://proxy.local:1080 -F URL
```
