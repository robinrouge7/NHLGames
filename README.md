# NHLGames
Tool to watch NHL games in High Definition
- Choose a date using the calendar or the left/right arrow.
- Choose a game you want to watch.
- Click on a stream link inside the game frame.
- Enjoy the game.

![image](https://cloud.githubusercontent.com/assets/23088305/25556664/43f875b0-2cce-11e7-8ca9-9f6d9d1b2121.png)

## Index
* [First use](#first-use)
  * [Message about the hosts file](#message-about-the-hosts-file)
  * [Setup](#setup)
     * [Hosts file](#hosts-file)
  * [Requirements](#requirements)
 * [User interface](#user-interface)
   * [Games](#games)
      * [Navigation bar](#navigation-bar)
      * [Game frame](#game-frame)
   * [Settings](#settings)
     * [Players](#players)
     * [Streamlink](#streamlink)
     * [Hosts](#hosts)
     * [Resolution](#resolution)
     * [Content Delivery Network (CDN)](#content-delivery-network-cdn)
     * [Other options](#other-options)
   * [Console](#console)
   * [Ad Detection Modules](#ad-detection-modules)
* [Chromecast](#chromecast)
* [Contribute](#contribute)


# First use
## Message about the hosts file
First time you start NHLGames it will ask you if you wish to view the Hosts file. That's mean the app has changed a system file to let you use NHLGames without issues by adding a line like this one `XXX.XXX.XXX.XXX www.hosting.site.com` at the end of it. If you want to view the changes, then click Yes and you will have to select Notepad to view the file. If NHLGames did not succesfully changed this file, see the [hosts file](#host-file) section.

## Setup
To be able to play streams properly, you have to choose a media player in the ![image](https://cloud.githubusercontent.com/assets/23088305/25557243/ce306f64-2cdb-11e7-9fa3-a4a73161c3ea.png) tab. Make sure the player that you choose has a valid path to the EXE file.

MPV player comes with NHLGames. So if you don't have or want VLC/MPC players, just use our default media player to stream games. Make sure you select mpv as the default player.

If you want to changes some settings, see the [Settings](#settings) section.

### Hosts file
To test your hosts file, go to Settings and press on `Test Hosts File` button. It should tell you if everything is fine.

If NHLGames is not set properly, press on `Open Hosts File` and select Notepad to open it, or go to `C:\Windows\System32\Drivers\etc` and open `hosts` using Notepad. Go at the end of the file and make sure that our entry is there. You can find the entry in the Settings tab next to the Hosts buttons. If you don't find it, you will have to add it manually (if NHLGames don't have access to it) or try `Add Hosts entry` button.

## Requirements
NHLGames is an app builded on .Net Framework 4.6. So, it's only available on Windows. If you run NHLGames on a Windows older than Windows 8 you will probably need to install [.Net Framework 4.6](https://www.microsoft.com/en-ca/download/details.aspx?id=30653)

# User interface
Everytime you launch NHLGames it will search for today's games. 

## Games
### Navigation bar
If you want to watch past games, use the calendar or use the arrows to navigate through the days.
![image](https://cloud.githubusercontent.com/assets/23088305/25556865/0f4cc51e-2cd3-11e7-96db-b875a4ab716c.png)
Use the refresh button (at the right) to refresh the current day games.

### Game frame
Here are 5 differents game frame colors that you will see while using NHLGames.
  1. Dark Grey : Upcoming games
  2. Blue : Today's games
  3. Green : Pre game
  4. Red : In progress
  5. Grey : Final games
  
  Note : 6th image shows the possibility to add live score or final score to the frame. You can turn it on/off in Settings tab.
  
![image](https://cloud.githubusercontent.com/assets/23088305/25557145/66d2a94c-2cd9-11e7-90ef-7e04e740f5a7.png)

## Settings
### Players
NHLGames supports 3 media players:
- MPV (default player, comes with NHLGames)
- MPC 
- VLC (version 2.2.4, 64 bits recommended)

If you don't have or want VLC/MPC players, use our default media player to stream games. Make sure you select mpv as the default player.

If you had previously installed VLC or MPC, NHLGames should find it automatically if you installed it in the default folder `Program Files`, otherwise you will have to browse ![image](https://cloud.githubusercontent.com/assets/23088305/25557239/b99ec37a-2cdb-11e7-8c27-d8b563128e8d.png) your computer and get the path to the EXE file. 

If you don't have one of these players installed and you want to install it, use the links on the right to download it.

### Streamlink
Streamlink is not a media player, it's an application that NHLGames use to get the stream from Internet and parse it to your media player. The path to streamlink.exe is inside NHLGames directory and it should not move, otherwise you will have to get the new path to it or you will get a message box that NHLGames lost the path and won't be able to play streams.

### Hosts
See the [hosts file](#host-file) section.

### Resolution
The selected value will defined which quality will be sent to your media player, from the lowest (224p) to the highest quality (720p at 60fps). Selecting the highest quality also means bigger files to download :

- 224p is about 300 Mo per hour
- 228p is about 500 Mo per hour
- 360p is about 700 Mo per hour
- 504p is about 950 Mo per hour
- 540p is about 1.30 Go per hour
- 720p is about 1.80 Go per hour
- 720p at 60fps is about 2.50 Go per hour

### Content Delivery Network (CDN)
Level 3 :
```
Level 3 owns and operates a global Tier-1 network and - logically - their CDN runs on top of it. 
Level 3 CDN has POPs on all continents and their product focus is on video and large object delivery. 
Level 3 CDN is part of the Google Cloud CDN Interconnect.
```

Akamai :
```
Akamai is one of the oldest CDNs and generally considered to be the largest global CDN. 
They have 'servers everywhere' and a wide range of products and services. 
The company is actively involved in Let's Encrypt and is pushing HTTP/2 adoption.
```

### Other options
If you wish to use these other options make sur you check `Enable` first.
- Output : Path where you want to save games as .mp4 files.
- Player args : If you want to add more arguments (commands) to be sent to your media player with the default args that NHLGames send.
- Streamer args :  If you want to add more arguments (commands) to be sent to streamlink with the default args that NHLGames send.

## Console
Go to this section to inspect everything that NHLGames does. Also, any error or warning will show here.

## Ad Detection Modules
NHLGames don't use any Ad Detection modules by default, but you can activate one by checking `Enabled` and by moving a module from the left box to the right. Select one and use the `>>>` arrow button to activate it, use the `<<<` arrow button to desactivate it. If you don't use any, it's better if you disable the Ad Detection module. 


# Chromecast
NHL Games don't support Chromecast, by Google Chrome does. Follow those steps if you want to play the game on your TV.

![image](https://cloud.githubusercontent.com/assets/23088305/25557771/3570cf2a-2ce6-11e7-980a-b605b93c66dc.png)

3. Select a pc monitor you want to share. Make sure audio share is checked.

![image](https://cloud.githubusercontent.com/assets/23088305/25556591/3145542a-2ccd-11e7-8ba4-d4947e2bb84f.png)

4. Use NHLGames to get a stream, once the game plays, move the media player window to the right monitor and enjoy the show.

![image](https://cloud.githubusercontent.com/assets/23088305/25556617/a6caab1e-2ccd-11e7-89d3-c9177a997ed1.png)

# Contribute
NHLGames is written in Visual Basic. Ad Detection modules are written in C#. We use Visual Studio to code. 

If you want to contribute :
- Fork the project and submit a pull request to `NHLGames\master` branch.
- Open an issue and tell us what's wrong with NHLGames.

NHLGames use also these NuGet packages:
- MetroModernUI
- CSCore
- Newtonsoft JSON .NET
- Prism.Core
