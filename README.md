---
module: React

level: 1

methods:
  - team
  - pair
  - solo

tags:
  - react
---

# Academy Project: TV Shows

<a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-nd/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/">Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License</a>.

## Overview

You must make a React app which shows details of all of the episodes of a TV show.

The episode data will come from [TV Maze](http://www.tvmaze.com/).

## About the episode data

### Where do I get the episode data from?

Initially, you will manually save data from their [API](http://www.tvmaze.com/api) (specifically [this link](https://api.tvmaze.com/shows/82/episodes)) to a JSON file in your project source.

In later exercises you will be challenged to have your app dynamically `fetch` the data from the API.

In all cases, you will be working with an array of objects, each of which represents an episode of a TV show.

### What does the episode data look like?

Here's an excerpt of [this file](https://api.tvmaze.com/shows/82/episodes) showing an example of ONE episode from the list.

```js
{
    id: 4952,
    url: "https://www.tvmaze.com/episodes/4952/game-of-thrones-1x01-winter-is-coming",
    name: "Winter is Coming",
    season: 1,
    number: 1,
    type: "regular",
    airdate: "2011-04-17",
    airtime: "21:00",
    airstamp: "2011-04-18T01:00:00+00:00",
    runtime: 60,
    rating: { average: 8.4 },
    image: {
      medium:
        "https://static.tvmaze.com/uploads/images/medium_landscape/1/2668.jpg",
      original:
        "https://static.tvmaze.com/uploads/images/original_untouched/1/2668.jpg",
    },
    summary:
      "<p>Lord Eddard Stark, ruler of the North, is summoned to court by his old friend, King Robert Baratheon, to serve as the King's Hand. Eddard reluctantly agrees after learning of a possible threat to the King's life. Eddard's bastard son Jon Snow must make a painful decision about his own future, while in the distant east Viserys Targaryen plots to reclaim his father's throne, usurped by Robert, by selling his sister in marriage.</p>",
    _links: { self: { href: "https://api.tvmaze.com/episodes/4952" } },
}
```

## Setup

- Create a new React app called `tv-shows` by using the [Academy simplified CRA starter app](https://github.com/WeAreAcademy/academy-react-starter).   

[Guide to React project creation setup (with TypeScript)](https://www.notion.so/weareacademy/How-to-create-a-React-app-with-TypeScript-76643f84db564a69a04db9a0b6a2f2e7)

- Set up continuous deployment of your app to [Netlify](https://netlify.app/) as `academy-yourgithubusername-tv-shows`.netlify.app.  [Netlify deployment guide for React apps](https://www.notion.so/weareacademy/How-to-deploy-a-React-app-to-free-Netlify-hosting-9e6ebd4dcb814cb483c34eb0f05ea96e)

### Setup - get the episode data:

- Download the episode data for the show "Game Of Thrones" from TV Maze API using this URL:
  https://api.tvmaze.com/shows/82/episodes

- Save the file as `episodes.json` in your project's `src` directory

- If your JSON data is all on one long line, you can run the editor command `format document`* to make it more readable. (*from the vscode command palette, ctrl-shift-p / cmd-shift-p).

- Edit your project's `tsconfig.json` and ensure you have the following property inside the section called compilerOptions: `"resolveJsonModule": true`

- Import the JSON data into a variable at the top of your `App.tsx` as follows:

```import episodes from './episodes.json'```

- Check the import was successful by adding the following after the import and checking the browser's console when the app loads.

```
console.log(`Imported ${episodes.length} episode(s)`);
console.log(`First episode's name is ${episodes[0].name}`);
```

- Once you've built a relevant React component to display the list of episodes, pass the `episodes` array to it as a prop.

- Use the following type when passing around an episode.  Note: It includes some intentional imperfections which you may need to address later in the exercise.

```
interface IEpisode {
  id: number;
  url: string;
  name: string;
  season: number;
  number: number;
  type: string;
  airdate: string;
  airtime: string;
  airstamp: string;
  rating: { average: number };
  runtime: number;
  image: {
    medium: string;
    original: string;
  };
  summary: string;
  _links: { self: { href: string } };
}
```

If you have to pass around a list of such episodes the type will be `IEpisode[]`.

### Rules about the episode data

You MUST NOT edit the static episode data. If you find that the data is unsuitable (e.g. fields are missing, or have unwanted characters), you should improve your own code so that _it_ can deal with such issues at run-time.

Why? If your app is later extended to allow the downloading of episode data for any one of hundreds of possible shows, frequently updated, tidying the data by hand will NOT be a feasible solution!  It's important to learn how to write code that can handle inconsistencies in data.

## Project Levels

This project is broken into various levels:

- [level 100](./level-100.md)
- [level 200](./level-200.md)
- [level 300](./level-300.md)
- [level 350](./level-350.md)
- [level 400](./level-400.md)
- [level 500](./level-500.md)
- [level 999 (further work)](./level-999.md)
