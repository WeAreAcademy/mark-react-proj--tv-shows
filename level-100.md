# Minimal features for level 100

1. All episodes must be shown
1. For each episode, AT LEAST the following must be displayed:
   1. the episode's name
   1. the season number (see below)
   1. the episode number (see below)
   1. the episode's medium-sized image
   1. the episode's summary text (see below)
1. Season number and episode number should be displayed as an **episode code**:
   1. Each part should be zero-padded to two digits.
   1. Example: `S02E07` would be the code for the 7th episode of the 2nd season. `S2E7` would be _incorrect_.
1. The page should state somewhere that the data has been obtained from [TVMaze.com](https://tvmaze.com/), and should link back to that site (or the specific episode on that site). See [tvmaze.com/api#licensing](https://www.tvmaze.com/api#licensing).

### Optional features at this point
* The summary text of some episodes contains what seem to be HTML tags (e.g. `<p>`).  Try to omit these tags when displaying the summary text.

## Screenshot of minimal version

Note: Provided your project meets the above requirements, it can **look** however you want.

Here is one example layout.

![example screenshot of level 100 showing list of episodes](./example-screenshots/example-level-100.png)

[top](./readme.md) - [level 200 >>](./level-200.md)
