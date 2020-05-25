# lastfm random artists' fetcher
Web application to fetch a random list of artists from a lastfm user library

This little web app was made to help me select a list of randam artists from my own lastfm library. It's usefull when you have a large library and can't remember all the artists you've listened to or can't decide what to listen next. 

As a Google Play Music (GPM) user and future YT Music user, there's no official APIs to automatically generate playlists. So I just made a little tweak using android automation app [Takser](https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm) to save a few clicks and open the bands the app returned directly on GPM.

## Configuring the web app
Just rename the file **params.ini.template** to **params.ini** and configure the parameters bellow:
```
user       =
apiKey     =
```
> You don't need to use **' '** or **" "**, just add the values after the **=** without spaces.

**user** parameter is the user of your account or someones else you wold like to obtain infomration of the library

**apiKey** parameter is the lastfm developer key to use it's APIs. It can be generated [here](https://www.last.fm/api/account/create)

## Usgin the web app
![setup](https://imgshare.io/images/2020/05/25/Capture01.png)
![results](https://imgshare.io/images/2020/05/25/Capture02.png)

## Using Tasker
You will notice that all artists urls are pointing something like tasker://Iron Maiden, this is a internal url that can be intercepted by tasker and execute the script to automatically open this artist on GPM.
To use this tasker project, you just need to import the file **tasker/LastFm.prj.xml** on your Tasker app. 
To use the entire project you will need the following apps:
- [Tasker](https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm) (Required)
- [AutoApps](https://play.google.com/store/apps/details?id=com.joaomgcd.auto) (Required)
- [AutoTools](https://play.google.com/store/apps/details?id=com.joaomgcd.autotools) (Optional - you can adapt a simpler version of the project to not use this plugin)
> Don't forget to enagle the option **Allow Phone Access** inside scene, otherwise the webview cannot load javascript resources and point the scene to the correct url where you are hosting the web app.

For further information about how you can use and configure Tasker and it's plugins, you can find a lot of tutorials and help in https://joaoapps.com/
