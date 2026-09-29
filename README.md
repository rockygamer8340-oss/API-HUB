<div align="center">

# api hub

**Every free API, one search away.**

Search 99 free APIs by what you're building (anime, game, weather, AI, crypto…), copy any endpoint in one tap, and start coding. APIs that need no key always come first.

[**Live site**](https://guileless-fox-39ed10.netlify.app)

</div>

![Sign-up page](screenshots/signup.png)

## Features

- **Search by topic.** Type `anime` and get Jikan, AniList, Waifu.pics and more. Type `game` and get PokéAPI, FreeToGame, Valorant, RAWG and others.
- **Fastest first.** 68 APIs work with no key at all and are always listed at the top. Next come APIs with an official public test key (NASA, TheSportsDB, TheMealDB), then APIs that need a free key.
- **One-tap copy** for every endpoint, example request and public key.
- **Your own keys, filled in.** Paste a key into a card and the example URL updates. Keys stay in your browser only.
- **Real accounts** with email and password, mobile OTP or Google, powered by Firebase Authentication.
- **16 categories:** anime, games, movies and TV, music, weather, crypto and finance, AI, images, fun, sports, food, science and space, news, books and words, developer tools, and places.

| Home | Search on phone |
| --- | --- |
| ![Home](screenshots/desktop-home.png) | ![Search](screenshots/phone-search.png) |

## Why no private keys?

Most API keys are personal. They belong to one account, and sharing them breaks the provider's terms and gets them blocked. So API Hub lists the no-key APIs ready to use, the official public test keys, and a direct link to get your own free key for everything else.

## Tech

- One `index.html` file with no build step
- React 18 with [htm](https://github.com/developit/htm), Framer Motion and Tailwind CSS (compiled and inlined)
- Firebase Authentication (compat SDK 10.14.1)
- Fonts: Instrument Serif, Barlow and Readex Pro

## Run it yourself

1. Download `index.html` and open it in a browser. That's it.
2. To use your own Firebase project, search `window.FIREBASE_CONFIG` inside `index.html` and replace the values with your web app config from **Firebase console › Project settings › Your apps**.
3. In Firebase, turn on **Email/Password**, **Google** and **Phone** under **Authentication › Sign-in method**.
4. Add your site's domain under **Authentication › Settings › Authorized domains**.

> Real SMS for phone login needs the Firebase Blaze plan. Email and Google login are free.

## Deploy

**GitHub Pages:** upload `index.html` to a public repo, then go to **Settings › Pages**, pick the `main` branch and click **Save**. Then add `your-username.github.io` to the Firebase authorized domains.

**Netlify:** drag the folder with `index.html` onto [app.netlify.com/drop](https://app.netlify.com/drop).

## Add an API

The catalog is the `APIS` array inside `index.html`. Each row looks like this:

```js
["Name", "Category", "n|d|k", "Description", "Base URL", "Example URL (use {KEY} for the key)", "Docs or sign-up URL", "search tags", "public key (only for d)"]
```

`n` = no key, `d` = public test key, `k` = free key required.

## Credits

Data comes from each API's own provider. API Hub only links to them. Made by rishu.
