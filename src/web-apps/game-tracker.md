# Game Tracker

**The gist**: build a web app and API for keeping track of your game library.

What you're playing, what you've finished, what you want to play. They're all really fun things to track. And organizing one's collection digitally scratches a certain collector's itch.

This app could be pretty simple to start, and it could expand in its complexity pretty organically.

No clever names for this project yet!

## Mock-Ups

![Game Tracker mobile mock-ups. First view: horizontally-aligned logo/title and "Account" link, "Brett's collection" heading, "Currently Playing" list and "Add Game" button, table with breakdown by platform and various columns. Second view: "Add Game" form with title, platform, play status and notes inputs, plus an "Add Game" button](./img/game-tracker.webp)

## Specs

- Authentication (user sign up)
- Add games to library
  - Platform
  - Play Status (unplayed, started, playing, finished, abandoned)
  - Notes
- Render library
  - By platform
  - By completion

## Extra Credit

- Support rating and writing review thoughts on each game
- Favorites list
- Add friends
- Pull in image data for games
- This doesn't have to be for games! It could be for any media, really.
- Badges based on collection size, completion rate, etc.
- Expand game metadata (playtime, region, ownership status, etc.)
- Steam import

## Tech Thoughts

This project would be a great candidate for building a rich GraphQL API that clients can consume. This would allow the web app to consume it and have a nice experience for managing one's library. And it would allow for mobile app clients to exist to manage what one's playing on the go.

I think an open-source, community-driven project like this could really thrive.

## Additional Thoughts

The desire is instantly there to try to make this platform contain a comprehensive database of games for all platforms, regions, etc. That's a huge project. One of the beautiful things about Backloggery it's so simple and doesn't include that. Sure you have to enter details manually, but having that control is quite nice and I think makes it easier to manage.

Maybe there's some middleground where auto-complete can be used for existing entries? I'm not quite sure. The manual entry is clearly easier for starting out though.

## References

- [Backloggery](https://www.backloggery.com) — very much the inspiration for this idea; simple and effective UI with great stats
- [Letterboxd](https://letterboxd.com) — movie tracking app
- [Discogs](https://www.discogs.com) — music tracking
- [How Long to Beat](https://howlongtobeat.com)
- Goodreads — book tracking app

## See Also

- [Media Log](../websites/media-log.md)
