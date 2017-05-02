## headless-jd2-docker

JDownloader 2 Headless Container with my.JDownloader.org Connection

## getting-started
1. Create a folder on your (docker)-host for the configuration files (eg. mkdir /config/jd2) and one for the downloads
e.g. /downloads
2. run `docker run -d --name jd2 -v /config/jd2:/opt/JDownloader/cfg -v /downloads:/opt/downloads benst/headless-jd2-docker`
3. stop the container `docker stop jd2`
4. You have to edit the config files to connect to the my.jdownloader.org Webservice. You will find the files after the first Container start in the config directory. Here: `/config/jd2/*json`
5. On your (docker)-host, add your credentials to the file `org.jdownloader.api.myjdownloader.MyJDownloaderSettings.json` as in `{ "password" : "password", "email" : "email@example.com", }` and if you like your DeviceName(the name jdownloader will show in the WebGui) `{  "devicename" : "foobar", }`
6. and change default Download Location in the file `org.jdownloader.settings.GeneralSettings.json` as in `{ "defaultdownloadfolder" : "/downloads" }`
7. start the container `docker start jd2`
8. you can jump into the container with: `docker exec -it <containerName> bash` and then look into /opt/Jdownloader/logs it takes about one Minute to finish the extraction if your Webinterface needs a little Time before you see something
9. if you like to use `docker-compose` then there is a compose file in the repo which you can use. Just edit the config according to the documentation inside.
