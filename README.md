# SceneRadio M3U

**English** · [Nederlands](README.nl.md)

An automatically updated M3U list of Dutch national, regional and DAB+ radio stations, with logos. Made for the Android app **SceneRadio**, but usable in any player that understands M3U lists with `tvg-logo` and `group-title`.

## Usage

The address of the list:

```
https://raw.githubusercontent.com/onneau/sceneradio-m3u/main/nederlandse-radio.m3u
```

- **SceneRadio**: the list is the default list. No account or token is needed.
- **Other players**: add the address above as a playlist or "M3U URL".
- The logos are in `logos/` and are named relatively in the list (`tvg-logo="logos/<name>.jpg?v=<code>"`). Players that do not understand relative addresses put `https://raw.githubusercontent.com/onneau/sceneradio-m3u/main/` in front of it.
- GitHub keeps raw files in its cache for a few minutes, so a new version can take a moment.

## What is in it

| File | Contents |
| --- | --- |
| `nederlandse-radio.m3u` | the list: name, genres (`group-title`, several separated by `;`), logo and stream address |
| `logos/*.jpg` | logos, at most 500 points on the longest side |
| `logos/manifest.json` | the source of each logo |

## How the list is made

This repository only contains the **result**. The list is made and checked automatically from a separate source list of its own:

- Streams are checked daily. A station only drops out of the list after failing three times in a row, and comes back by itself as soon as the stream works again.
- Logos come from Wikimedia Commons, from the stations themselves or from the [Radio Browser](https://www.radio-browser.info) database.
- Changes to this repository are made by the maintainer; changes made here by hand are overwritten at the next update.

## A station is missing or does not work?

Create an *issue* with the name of the station and, if you have it, the address of the stream.

## No connection with the stations

This project is in no way affiliated with, sponsored by or endorsed by the radio stations, broadcasters or companies whose name, logo or stream appears in the list. All names and logos are the property of their owners and are only used to make a station recognizable. There is **no audio** in this repository: the streams are fetched directly from the stations.

**Does a rights holder want a name, logo or stream removed from here?** Report it via an *issue* or via https://github.com/onneau. It will be removed as soon as possible.

## License

The list and the texts fall under the [PolyForm Noncommercial License 1.0.0](LICENSE): use for private, hobby, research, education and charities, not commercial. See `NOTICE` ([Nederlands](NOTICE.nl.md)) for what is not covered (the logos and names of the stations).
