<p align="center">
  <a href="https://sponsor.ajay.app"><img src="public/icons/LogoSponsorBlocker256px.png" alt="Logo"></img></a>
  
  <br/>
  <sub>Logo by <a href="https://github.com/munadikieh">@munadikieh</a></sub>
</p>

<h1 align="center">SponsorBlock for Safari (MacOS)</h1>
<p align="center"><a href="https://apps.apple.com/au/app/sponsorblock-port-for-youtube/id1532163541"><img src="https://raw.githubusercontent.com/rakalix/SponsorBlock/master/public/Download_on_the_Mac_App_Store_Badge_US-UK_RGB_blk_092917.svg"></a> </p>

<p align="center">
  <b>Download:</b>
  <a href="https://chrome.google.com/webstore/detail/mnjggcdmjocbbbhaepdhchncahnbgone">Chrome/Chromium</a> |
  <a href="https://addons.mozilla.org/addon/sponsorblock/?src=external-github">Firefox</a> |
  <a href="https://github.com/ajayyy/SponsorBlock/wiki/Android">Android</a> |
  <a href="https://github.com/ajayyy/SponsorBlock/wiki/Edge">Edge</a> |
  <a href="https://sponsor.ajay.app">Website</a> |
  <a href="https://sponsor.ajay.app/stats">Stats</a>
</p>

<p align="center">
  <b>Unofficial Ports:</b>
  <a href="https://github.com/ajayyy/SponsorBlock/wiki/Unofficial-Ports#mpv-media-player">MPV</a> |
  <a href="https://github.com/ajayyy/SponsorBlock/wiki/Unofficial-Ports#kodi">Kodi</a> |
  <a href="https://github.com/ajayyy/SponsorBlock/wiki/Unofficial-Ports#ios">iOS</a> |
  <a href="https://apps.apple.com/us/app/sponsorblock-port-for-youtube/id1532163541">Safari (MacOS)</a>
</p>

<p align="center">
    <a href="https://addons.mozilla.org/addon/sponsorblock/?src=external-github"><img src="https://img.shields.io/amo/users/sponsorblock?label=Firefox%20Users" alt="Badge"></img></a>
    <a href="https://chrome.google.com/webstore/detail/mnjggcdmjocbbbhaepdhchncahnbgone"><img src="https://img.shields.io/chrome-web-store/users/mnjggcdmjocbbbhaepdhchncahnbgone?label=Chrome%20Users" alt="Badge"></img></a>
    <a href="https://sponsor.ajay.app/stats"><img src="https://img.shields.io/badge/dynamic/json?label=Submissions&query=totalSubmissions&suffix=%20segments&url=http%3A%2F%2Fsponsor.ajay.app%2Fapi%2FgetTotalStats&color=darkred" alt="Badge"></img></a>
    <a href="https://sponsor.ajay.app/stats"><img src="https://img.shields.io/badge/dynamic/json?label=Contributing%20Users&query=userCount&url=http%3A%2F%2Fsponsor.ajay.app%2Fapi%2FgetTotalStats&color=darkblue" alt="Badge"></img></a>
    <a href="https://sponsor.ajay.app/stats"><img src="https://img.shields.io/badge/dynamic/json?label=Time%20Saved%20From%20Skips&query=daysSaved&url=http%3A%2F%2Fsponsor.ajay.app%2Fapi%2FgetDaysSavedFormatted&color=darkgreen&suffix=%20days" alt="Badge"></img></a>
</p>



SponsorBlock is an open-source crowdsourced browser extension to skip sponsor segments in YouTube videos. Users submit when a sponsor happens from the extension, and the extension automatically skips sponsors it knows about. It also supports skipping other categories, such as intros, outros and reminders to subscribe.

It also supports Invidio.us.

**Translate:** [![Crowdin](https://badges.crowdin.net/sponsorblock/localized.svg)](https://crowdin.com/project/sponsorblock)

# Important Links

See the [Wiki](https://github.com/ajayyy/SponsorBlock/wiki) for important links.

# Donate to cover Apple's US$99 developer fees

<b>Donate with PayPal:</b>   [![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=HTXQKVQJ3VZQY)

<b>Donate with <img src="https://upload.wikimedia.org/wikipedia/commons/c/c5/Bitcoin_logo.svg" width="153" height="32"><br>bc1q46esknq8n9yrqms92973nc8u9ds4nm4nuvt85v</b>

<b>Donate with <img src="https://upload.wikimedia.org/wikipedia/commons/2/2d/Monero-Logo.svg" width="141" height="37"><br>8AZJ9NsYVfVE6uGc3irxHmTDGq93FoTDnFjvoaG43dzbR9k2LgwJ7MSWHngdZLEGhrCkLy5KXAShugaFzsQ77JQb6bJyrCR</b>

# Server

The backend server code is available here: https://github.com/ajayyy/SponsorBlockServer

It is a simple SQLite database that will hold all the timing data.

To make sure that this project doesn't die, I have made the database publicly downloadable at https://sponsor.ajay.app/database.db ([License](https://github.com/ajayyy/SponsorBlock/wiki/Database-and-API-License)). If you are planning on using the database in another project, please read the [API Docs](https://github.com/ajayyy/SponsorBlock/wiki/API-Docs) page for more information.

The dataset and API are now being used in some [ports](https://github.com/ajayyy/SponsorBlock/wiki/Unofficial-Ports) as well as a [neural network](https://github.com/andrewzlee/NeuralBlock).

A [previous project](https://github.com/Sponsoff/sponsorship_remover) attempted to create a neural network to predict when sponsored segments happen. That project is sadly abandoned now, so I have decided to attempt to revive this idea starting from a crowd-sourced system instead.

# API

You can read the API docs [here](https://github.com/ajayyy/SponsorBlockServer#api-docs).

# Building

Rename `config.json.example` to `config.json` and adjust configuration as desired.

There are also other build scripts available. Install `npm`, then run `npm install` in the repository to install dependencies. 

Run `npm run build` to generate a Chrome extension.

Use `npm run build:firefox` to generate a Firefox extension.

The result is in `dist`. This can be loaded as an unpacked extension

## Developing with a clean profile

Run `npm run dev` to run the extension using a clean browser profile with hot reloading. Use `npm run dev:firefox` for Firefox. This uses [`web-ext run`](https://extensionworkshop.com/documentation/develop/web-ext-command-reference/#commands).  
Known chromium bug: Extension is not loaded properly on first start. Visit `chrome://extensions/` and reload the extension.


### Attribution Generation

If you contribute and add a dependency, update the attribution file using the following steps:

Make sure the attribution generator is installed: `npm i -g oss-attribution-generator`

```bash
generate-attribution
mv ./oss-attribution/attribution.txt ./public/oss-attribution/attribution.txt
```

# Credit

The awesome [Invidious API](https://github.com/omarroth/invidious/wiki/API) was previously used.

Originally forked from [YTSponsorSkip](https://github.com/NDevTK/YTSponsorSkip), but zero code remains.

Some icons made by <a href="https://www.flaticon.com/authors/gregor-cresnar" title="Gregor Cresnar">Gregor Cresnar</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a> and are licensed by <a href="http://creativecommons.org/licenses/by/3.0/" title="Creative Commons BY 3.0" target="_blank">CC 3.0 BY</a>

Some icons made by <a href="https://www.flaticon.com/authors/freepik" title="Freepik">Freepik</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a> are licensed by <a href="http://creativecommons.org/licenses/by/3.0/" title="Creative Commons BY 3.0" target="_blank">CC 3.0 BY</a>
