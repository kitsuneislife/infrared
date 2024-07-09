<img align="left" width="70px" src="https://raw.githubusercontent.com/titaniumnetwork-dev/Holy-Unblocker/master/views/assets/img/icon.png"></img>
# Holy Unblocker LTS (v6.x.x)

Holy Unblocker LTS, an experimental web proxy service, can bypass web filters or 'blockers' regardless of whether the method of censorship is client-side or network-based. This includes the potential ability to bypass content blockers overseas, Chrome extensions, localized client firewalls, and network-related filters.

This project serves mostly as a proof of concept for the ideal clientless solution to bypassing censorship. Being a secure web proxy service, it supports numerous sites while being updated frequently and concentrating on detail with design, mechanics, and features.

Works with a large number of sites, including YouTube, Discord, and more!
Also has a good amount of locally hosted games featured on the site.

#### Supports
- Youtube.com
- Discord.com
- Google.com
- Reddit.com
- Bing.com
- And more sites!

#### Features:
- Tab customization using the Options menu for improved stealth 
- Considerable variety with the open selection of proxy types 
- Game library with moderately decent titles
- Has frequent support articles for issues relating to the various proxy instances

<img src="https://raw.githubusercontent.com/titaniumnetwork-dev/Holy-Unblocker/master/views/assets/img/preview/hu-v6.1.0-preview.png"></img>

#### You can support Holy Unblocker by starring the repository!

Read below for information if the official site is blocked or for obtaining more links. Can't deploy using any of the free options below? Check out Railway or look into cheap, paid VPS hosting solutions.

**Be sure to join Titanium Network's Discord for more official site links:** <a href="https://discord.gg/unblock">https://discord.gg/unblock</a>

## Deploy Holy Unblocker

[![Deploy to Vercel](https://vercel.com/button)](https://vercel.com/import/project?template=https://github.com/QuiteAFancyEmerald/Holy-Unblocker)
[![Run on Replit](https://raw.githubusercontent.com/BinBashBanana/deploy-buttons/master/buttons/remade/replit.svg)](https://replit.com/github/QuiteAFancyEmerald/Holy-Unblocker)
[![Deploy to Azure](https://raw.githubusercontent.com/BinBashBanana/deploy-buttons/master/buttons/remade/azure.svg)](https://deploy.azure.com/?repository=https://github.com/QuiteAFancyEmerald/Holy-Unblocker)
[![Deploy to IBM Cloud](https://raw.githubusercontent.com/BinBashBanana/deploy-buttons/master/buttons/remade/ibmcloud.svg)](https://cloud.ibm.com/devops/setup/deploy?repository=https://github.com/QuiteAFancyEmerald/Holy-Unblocker)
[![Deploy to Amplify Console](https://raw.githubusercontent.com/BinBashBanana/deploy-buttons/master/buttons/remade/amplifyconsole.svg)](https://console.aws.amazon.com/amplify/home#/deploy?repo=https://github.com/QuiteAFancyEmerald/Holy-Unblocker)
[![Run on Google Cloud](https://raw.githubusercontent.com/BinBashBanana/deploy-buttons/master/buttons/remade/googlecloud.svg)](https://deploy.cloud.run/?git_repo=https://github.com/QuiteAFancyEmerald/Holy-Unblocker)

<details><summary>More Deployments</summary>

[![Deploy on Railway](https://railway.app/button.svg)](https://railway.app/new/template?template=https%3A%2F%2Fgithub.com%2FQuiteAFancyEmerald%2FHoly-Unblocker)
[![Deploy to Koyeb](https://www.koyeb.com/static/images/deploy/button.svg)](https://app.koyeb.com/deploy?type=git&repository=github.com/QuiteAFancyEmerald/Holy-Unblocker-Old&branch=master&name=HolyUnblocker&run_command=npm%start)
</details>

## Table of contents:

- [Setup](#how-to-setup)
    - [Structure](#structure)
        - [Structure Information](#structure-information)
        - [Static Files](#details-of-views)
        - [Scripts](#scripts-located-in-viewsassetsjs)
    - [Future Additions](#future-additions)
    - [Beginner's Explanation](#vauge-explanation-for-beginners-with-external-proxies-and-hosting)
      - [Hosting Providers](#list-of-some-good-hosting-options)
      - [Domain Setup](#freenomdomain-steps)
      - [Cloudflare Setup](#cloudflare-steps)
      - [Workspace Configurations](#workspace-configurations)
    - [Detailed FAQ](#detailed-faq)
    - [More Information](#more-information)

## How to Setup

Either use the button above to deploy to Heroku or do the below:

```
git clone https://github.com/titaniumnetwork-dev/Holy-Unblocker.git

cd Holy-Unblocker

npm install

npm start
```

The default place for the proxy when its started is `http://localhost:8080` but you can change it if needed in config.json

This website is hosted locally with Ultraviolet and Rammerhead built-in.


## Structure
<details><summary>Web Pages</summary>

- `index.html`: The homepage of the site.
- `404.html`: The 404 page.
- `error.html`: Other errors that are not 404.
- `info.html`: Documentation (This page!)
- `faq.html`: Frequently asked questions page.
- `hidden.html`: Fake "Site not Found" page (unused)
- `frame.html`: Handles any pages under stealth.
- `surf.html`: Web Proxies page, page offers to be redirected to any proxies you would like to add. In this case, Corrosion, Womginx, and Palladium.
- `credits.html`: List of all contributors to the site.
- `bookmarklets.html`: Bookmarklets page, to be worked on more in the future.
- `icons.html`: Information regarding Settings Menu page. Added this in for standard users.
- `terms.html`: Terms of Services, AUP and Privacy Policy page.
- `gtools.html`: Games page, help from @BinBashBanana and @kinglalu.
- `games5.html`: HTML5 game navigation page.
- `emulators.html`: Emulator navigation page, using <a href="https://github.com/BinBashBanana/webretro">webretro</a>.
- `emulibrary.html`: Games page for emulated games (not included in public release)
- `flash.html`: Games page for flash games, credits given to @BinBashBanana and Titanium Network for its assets.
- `ultraviolet.html`: TODO
- `rammerhead.html`: TODO
- `youtube.html`: An proxied version of Youtube running off of the locally hosted Corrosion.
- `discord.html`: Hub for the Discord proxy.
- `reddit.html`: Hub for the Reddit proxy.
</details>

### Structure Information
- `/views/`: The physical site base of Holy Unblocker goes here where static assets are served.
- `/src/`: For future implementation of obfuscation and keyword removing features.

#### Details of `/views/`
- `/archive/` is used for game pages and vibeOS.
- `/pages/` is used for the HTML for the site.
- `/assets/` is used for various assets for CSS, JS, and images.

#### Scripts located in `/views/assets/js/`
- `common.js` is used on all of the pages for common useful functions.
- `prset.js` is used on the proxy pages for proxy form functionality.
- `header.js` inserts the header into every page using javascript.
- `csel.js` manages the settings menu on the header.
- `footer.js` inserts the footer into every page using javascript.
- `gnav/*.js` are used for navigation on the games pages.

## Future Additions
This will be our nonexhaustive todo list for Holy Unblocker LTS v6.x.x and above.

### Code Cleanup

  - [ ] Remove the timestamps attached to the end of the JS file names.
  - [ ] Remove all current obfuscation in the source code. It needs to be dynamically obfuscated if anything, or not obfuscated at all. This option will be a config option on the server side before rendering with Express for a performance focus. Meta elements will have an additonal attribute indicating if they should be moved. This is to ensure a SEO source can be served by config or a source focused on pure censorship evasion.
  - [ ] Optimize the stylesheets and the HTML layout. Add more proper commenting and redivide the code so that it's less hard on the eyes.
  - [ ] Optimize the JS. This time it won't be in one line and will be somewhat thoroughly commented.
  - [ ] Restructure navigation scripts to ensure updated proxy functionality is sanitized and effective
  - [x] Particles.js automatically adjusting per display size

### Proxy Functionality
  - [x] Ensure Ultraviolet is updated to support bare-mux and wisp - done
  - [x] Add Rammerhead support - done
  - [ ] Fix slow Ultraviolet speeds despite being local; something on the backend??

### Site Redesign
  - [x] Landing Page - done
  - [ ] Web Proxies page
  - [ ] Application page
  - [ ] Games Libray page
  - [x] Footer Design - done
  - [x] Header Design

## Vauge Explanation for Beginners With External Proxies and Hosting
You will first want to host your proxies locally or externally. OUTDATED

#### List of some good hosting options:
- <a href="#">Oracle Cloud</a> (Free, Paid, Dedicated)
- <a href="https://repl.it">Repl.it</a> (Free)
- <a href="https://azure.microsoft.com">Azure</a> (Free and Paid)

Out of the list of hosting providers Dedipath and Azure rank first as a preference. You may also self-host.

After you have selected a decent VPS, use Cloudflare for the DNS records for both the site and the subdomains for the proxies.

This is an example of DNS records involving Heroku. Self-hosting will require `A records` preferably.
<img src="https://raw.githubusercontent.com/titaniumnetwork-dev/Holy-Unblocker/master/views/assets/img/dnssetup.png" width="500"></img>

- `@` and `www.example.ml` are being used for the local Ultraviolet proxy.
- `client.example.ml` is being used for Rammerhead.
- `a.example.ml` is being used for womginx.
- `cdn.example.ml` is being used for a private Ultraviolet host on the official sites.

As stated previously, Holy Unblocker is hosted locally with Ultraviolet.

#### Freenom/Domain Steps
For beginners, Freenom is a good provider for obtaining domains for free. However, Freenom only provides their TLDs (`.cf`, `.ml`, `.gq`, `.ga`, and `.tk`) for free, which can be easily blocked.

- Get some Freenom domains then add them to your Heroku instance (Personal > [App Name] > Settings > Domains)
Add a domain for both `www.example.cf` and `example.cf` with .cf being interchangeable with other Freenom domain names.
- If you prefer to obtain premium domains (TLDs) then use <a href="https://porkbun.com">Porkbun</a>, which offers domains for amazing prices. Literally a `.net` domain normally costs around $10. On Porkbun for the first year it costs $3 so its definitely a deal.

#### Cloudflare Steps
- Use Cloudflare (make an account), add your site (Freenom Domain or other) and then add your various DNS targets to Cloudflare. Make sure you add Cloudflare's Nameservers which will be given later when you are adding your site. 

Make sure they are CNAME although A records also work and try to follow this structure:

**Type | Name | Target**

`CNAME | @ | your-main-heroku-target-here.herokudns.com`  
`CNAME | www | your-main-heroku-target-here.herokudns.com`

**Below are if you want external proxies also with your site:**

`CNAME | a | your-womginx-instance-here.herokudns.com`  



Make sure HTTPS is forced and have SSL set to Flexible for some services. Otherwise you can have SSL set to Full.

#### Workspace Configurations 
Preferably if you have your own device use Visual Studio Code. Pretty much the best option you can get but obviously this is an opinion. Also make sure you have <a href="https://nodejs.org/">Node.JS</a> installed on your machine.

Not going to go too in depth with this part but first fork this repository. The clone it locally through a Terminal of some sort depending on what OS you are on. Make sure you navigate to the folder you want to set this up in.

```
git clone https://github.com/titaniumnetwork-dev/Holy-Unblocker.git

cd Holy-Unblocker

npm install
```

Now simply add the folder you cloned this repo in in VSC. Then run `npm install`. I recommend that if you are releasing this publically on GitHub that you add a `.gitignore` in your root directory with the following exclusions:

```
node_modules
```

Now you have your following workspace environment setup. To deploy the following workspace you just created you will need to look up depending on your hosting provider.

For an online IDE that you can use on your school computer and/or chromebook use GitPod. Basically the equivalent of Visual Studio Code but with in-browser support.
- Make an account: `https://gitpod.io/`
- Fork this repo and enter in this URL to setup your workspace: `https://gitpod.io#https://github.com/YourNameHere/Holy-Unblocker/`

Use the same steps above by running `npm install` in your repository and adding a `.gitignore` in your root directory specifying to exclude `node_modules`.

## Detailed FAQ
<details>
<summary>Quick FAQ</summary>

#### Where can I find the games for this repo? (404 errors, etc.)
Due to piracy concerns, size, etc. this has been moved over <a href="https://github.com/QuiteAFancyEmerald/HU-Archive">here</a>. EmuLibrary is not featured in the public version.

**Why is the site I am on not working correctly or having CAPTCHA errors?**

Captcha support is currently not available on all of the current proxies sadly. Therefore some sites may not work with any of the sites. Read below for issues with links on sites.

**I am getting 502 errors. What do I do?**

When this happens you may either switch sites to fix the error or wait a bit. Sometimes clearing your cache can help.

If you still have any questions feel free to ask them in the discord linked here.

</details>

### Why are official domains now numbered? Is this project maintained again?
Yes, this project is active again for LTS support! However, the approach is now much simpler to ensure functionality: traffic will be focused on a single domain. More than ever, this project serves as a proof of concept for the brave souls willing to innovate in the web proxy service space.

<details><summary>Former Closing Message (Original - 2022)</summary>

This isn’t the greatest announcement sorry. After lots of thought and severe hesitation I’m shutting down Holy Unblocker and leaving TN. It's just been something that I’ve been super conflicted with for months hence the lack of updates and the massive gaps that happened last year. I just didn’t want to throw away a project that I passionately enjoyed and spent time on while making amazing friends and meeting epic devs here. I could go on forever for who these people are but ima like leave it here. They know who they are :D

The main change of thought is that I’m finally just putting an end right now due to 1) the lack of motivation 2) the community is NOT the greatest at time and not the nicest at times (have to put that out here) 3) the future doesn’t look so good for HU/TN as a project.

Some things I’ll be keeping secret since there are more reasons to this choice unless otherwise for those who don’t find this enough information. Good friends here will know that I’ve been super stressed about this choice for months now. Also regardless a good motivator for this choice is the fact that I’ll be graduating soon.

It’s possible that I may continue/come back for this in the future or keep it on GitHub only. I leave this here because even now I am still doubting myself about this change. But for now I’d check out other proxy sites like Incognito (Duce DOES a ton of updates frequently and he is the creator/developer of Ultraviolet so give him some love) :yayy_hopi: 

Check out his Patreon also! For current HU patrons you will not be billed next month and the HU Patreon will be archived so head over to Duce’s patron so he can purchase more domains for Incognito.

With love <3
Emerald :HuTaoHype:

</details>


## More Information
This project is maintained by the Holy Unblocker LTS team and is an official flagship Titanium Network web proxy site.

- <a href="https://github.com/titaniumnetwork-dev/">https://github.com/titaniumnetwork-dev/</a>
- <a href="https://titaniumnetwork.org/">https://titaniumnetwork.org/</a>

View the official website for more detail and credits.

### Web Proxy Sources:
This project currently uses Ultraviolet, Wisp, Womginx, and Rammerhead, linked below.

- <a href="https://github.com/titaniumnetwork-dev/Ultraviolet">Ultraviolet</a>
- <a href="https://github.com/binary-person/womginx">Womginx</a>
- <a href="https://github.com/binary-person/rammerhead">Rammerhead</a>
- <a href="https://github.com/MercuryWorkshop/wisp-server-node">Wisp</a>
- <a href="https://github.com/MercuryWorkshop/bare-mux">Bare-Mux</a>
- <a href="https://github.com/tomphttp/bare-server-node">TOMP Bare Server</a>


### Other Dependencies:

- <a href="https://github.com/tsparticles/tsparticles">tsparticles</a>
- <a href="https://github.com/helmetjs/helmet">Helmet for Express</a>
- <a href="https://github.com/BinBashBanana/webretro">webretro</a>
- <a href="https://ruffle.rs/">Ruffle</a>
- <a href="https://github.com/michalsnik/aos">AOS</a>
- <a href="https://github.com/nordtheme">Nord Theme</a>
- <a href="https://fontawesome.com/">Font Awesome</a>

### Notable Mentions:

- <a href="https://soyoustart.com/">SoYouStart / OVH</a> (Hosting Provider)
