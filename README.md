# Twitch Giphy Bot Overlay

This will allow Twitch chat to use a custom command like: "!giphy cats". It will then search giphy for "cats" and display a random image from the results. 

## Requirements and notes

This project can run locally and does not require a server. Simply open giphy.html in a web browser. 

This requires a Giphy Account and Giphy API key.

- Head over to: https://developers.giphy.com/dashboard/ 
- Create a GIPHY API Key by clicking “Create an App” on the Developer Dashboard (you need to create an account first).
- Note: All API Keys start as beta keys, which are rate limited (42 reads per hour and 1000 searches/API calls per day.).
- Click on Create an App
- Select API
- Give your App a name and description.
- Click Create App. 

You should now have a API Key that can be used with this project.

## Install and use

- Open giphy.html in a text editor like notepad++
- Look for this section. 
```javascript
// Configuration - Settings
let twitchChannel = "MrCoolStreamer";
let twitchChatCommand = "!giphy";
let defaultImage = "";
let giphyApiKey = "api_key_goes_here";
let giphyRating = "r";
let giphyLang = "en";
let giphyLimit = 25;
let timeOut = 10;
```

**twitchChannel:** Required. Your Twitch channel name.

**twitchChatCommand:** Required. The Twitch chat command (!giphy cats)

**defaultImage:** Optional. This will set a background image. This could be an image that you want to display when no Giphy images are being played.

**giphyApiKey:** Required. You Giphy API key that you generated from https://developers.giphy.com/dashboard/

**giphyRating:** Giphy offers some ratings to filter images. (g, pg, pg-13, r).

**giphyLimit:** The number of images to randomly pick from. Max is 25 images.

**timeOut:** How long should the image stay on screen.

Once everything is configured and saved, you can now open giphy.html in your default web browser to test. 

Copy the URL from your browser to add it to OBS as a browser source... example: (file:///home/teklynk/twitch_giphy/giphy.html)