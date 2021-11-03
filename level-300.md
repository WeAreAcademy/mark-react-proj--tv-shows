# Level 300 - Add an Episode Selector

1. Complete all requirements from level 200
1. Add a `select` input which allows you to jump quickly to an episode:
   1. The select input should list all episodes in the format: "S01E01 - Winter is Coming"
   1. When the user makes a selection from the list, they should then ONLY be shown the selected episode.  Be sure to provide a way for the user to see all episodes again (e.g. by clicking a button).
1. Tidy up: if you haven't already then reconsider the episode summaries. The original data for the episode summaries contained html tags eg `<p>`. Remove these from the string before displaying the text.
1. Handle missing images: currently your data specifies an image for every episode but you will find you cannot rely on that when you move to live data later. For example, [here is the data from The Simpsons](https://api.tvmaze.com/shows/83/episodes) - if you search through it for `null` you'll sometimes see that future or very recent episodes have `image: null`.  Adapt your app to correctly handle this situation and use appropriate data to check it works.

## Example screenshot of Episode Selector

Note: Provided your project meets the above requirements, it can **look** however you want.

Here is one example layout.

![level 300 example showing episode selector](./example-screenshots/example-episode-selector.jpg)

[<< level 200](./level-200.md) - [top](./readme.md) - [level 350 >>](./level-350.md)
