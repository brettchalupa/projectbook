# Uptime Checker

**The gist**: build an app that allows a user to enter a URL for the app to check periodically to ensure it responds with a successful 2XX response; if not, email the user.

You know what stinks? When your websites or web apps go down. So let's build a web app that tells us when that happens. This project is pretty straightforward and has aspects different from other content-manage-y apps.

I'd probably call this project **Watchpup**! 🐶

## Specs

- Authentication (sign up, log in, log out)
- Add websites to check with a name and URL
- Check the website shared for a 200 response every 30 mins (can be less or more frequent)
- Log successful and unsuccessful checks so it's clear whether or not a check ran and how it went
- If the website is down, email the user the site is down

## Concepts

- Periodic job running
- HTTP requests

## Extra Credit

- Configurable frequency for checking

## References

- [Julia Evans' article "Monitoring tiny web services"](https://jvns.ca/blog/2022/07/09/monitoring-small-web-services/) — an exploration in building a simple uptime checker
- [UptimeRobot](https://uptimerobot.com/) — a legit version of an uptime checker you can use with a generous free plan
