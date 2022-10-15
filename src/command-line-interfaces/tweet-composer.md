# Tweet Composer

**The gist**: build a CLI that allows someone to easily compose a tweet for their Twitter account from their terminal.

Often when working or coding, I'd like to tweet something out but not fall down the rabbit hole of reading other people's tweets. It'd be nice if there was a way to send a tweet right from my terminal.

I'd call this program **toot**.

## Mock-Ups

The simplest version:

``` console
$ toot "I'm a little bit concerned with how much cereal I've been eating lately."
🦉 tweet posted, view: https://twitter.com/whatever/the/url/is
```

Extra Credit version for starting a thread of multiple tweets:

``` console
cat storm.txt | toot -
🦉 4 tweets posted, view: https://twitter.com/url/to/first/post
```

## Specs

- Get auth token from Twitter for the account
- Store it somewhere
- Integrate with the Twitter API to send the tweet
- Handle errors gracefully

## Concepts

- API integration
- Authentication for an account with an API

## Extra Credit

- Support multiple accounts and the ability to specify which one
- Read from stdin so that files can be used with `cat` or commands can be chained together
- Support sending multiple tweets as a thread in reply to one another from one text string by splitting up based on newlines or empty lines
- Spellcheck tweets before they get sent
- Expand to support more Twitter functionality if you really wanted, I guess
- Build it for another social network
