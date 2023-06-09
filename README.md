# refire-forum


<!-- social media connecting shield -->

[![Instagram][instagram-shield]][instagram-url]
[![Twitter][twitter-shield]][twitter-url]
[![LinkedIn][linkedin-shield]][linkedin-url]
[![Github][github-shield]][github-url]

![Github Banner](https://github.com/DynastyElvis/refire-forum/blob/master/src/Screenshot%20from%202023-04-13%2014-12-16.png)

<!-- contents of projects -->


<!-- my social media links -->

[instagram-url]: https://www.instagram.com/dynastyelvis/
[twitter-url]: https://twitter.com/Dev_Rono
[linkedin-url]: https://www.linkedin.com/in/kipkemoi-elvis-aa3548209
[github-url]: https://github.com/DynastyElvis

<!-- shield icon links -->


[email-shield]: https://img.shields.io/badge/-Email-black.svg?style=flat-square&logo=gmail&color=555
[chatbot-shield]: https://img.shields.io/badge/-Chatbot-black.svg?style=flat-square&logo=chatbot&color=555
[portfolio-shield]: https://img.shields.io/badge/-Portfolio-black.svg?style=flat-square&logo=portfolio&color=555

[instagram-shield]: https://img.shields.io/badge/-Instagram-black.svg?style=flat-square&logo=instagram&color=555&logoColor=white
[twitter-shield]: https://img.shields.io/badge/-Twitter-black.svg?style=flat-square&logo=twitter&color=555&logoColor=white
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=flat-square&logo=linkedin&colorB=555
[github-shield]: https://img.shields.io/badge/-Github-black.svg?style=flat-square&logo=github&color=555&logoColor=white

Serverless discussion forum built with React, Redux and Firebase using [refire](https://github.com/hoppula/refire) and [refire-app](https://github.com/hoppula/refire-app).

Base UI components are from excellent [Elemental UI](http://elemental-ui.com/).

## Live demo

[https://refire.firebaseapp.com](https://refire.firebaseapp.com)



## Features

* Categories, boards and threads
* Paging for boards and threads
* Quoting when replying to posts
* Thread and Post previews
* Markdown support
* Emoji support using `:emoji:` syntax :fire:
* User profile pages
* Login with Google, Facebook, Github & Twitter accounts
* Admin tools (delete threads & single posts, lock/unlock threads)
* CSS-in-JS styled components, fully themeable
* Dark & light color themes
* Upvoting single posts
* Users can edit their own posts

## Roadmap

* Allowing boards and threads to be bookmarked properly
* Search using redux-search
* Image attachment upload to Firebase
* Allowing users to edit their own thread titles
* Single post linking
* Show list of available emojis
* Sticky threads
* Thread and post tagging
* Notifications
* Reactions to posts with emojis
* Improved admin section
* Moderating
* User editable theme

## Deploying your own instance

1. Create your new app in [Firebase dashboard](https://console.firebase.google.com/)

2. Copy and paste `apiKey` from your Firebase app console's `Overview > Add Firebase to your web app` to `src/config.js`

3. Enable `Sign-in providers` you want to use in your Firebase app console's `Authentication > Sign-in method` settings

4. Change `projects.default` value to your app name in `.firebaserc`

5. Run `npm install` and `npm run build`

6. Run `npm run login` to login to Firebase

7. Run `npm run bootstrap` to copy the initial data structure to Firebase

8. Run `npm run deploy` to deploy the app and security rules to Firebase

## Running locally

`npm start` will start the development server on `localhost:4000`

## Adding admin users

Create `adminUsers` path in your Firebase and set your admin user's `uid` as key and `true` as value:

```
"adminUsers": {
  "google:123456789": true
}
```

## Customizing settings

You can edit default paging settings by changing `settings/BOARD_PAGE_SIZE`, `settings/THREAD_PAGE_SIZE` and `settings/THREAD_PAGE_LIMIT`.

You can configure date format by changing `settings/DATE_FORMAT`.

## Custom forum name

Export `siteName` in `./src/config.js`.

```js
export const siteName = "My forum"
```

## Security rules

Firebase security rules are defined in `security-rules.bolt`.

Use `npm run build:rules` to generate `security-rules.json` after making changes.

Use `npm run deploy:rules` to deploy security rules.

## License

MIT
