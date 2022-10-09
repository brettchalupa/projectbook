# Event Platform

**The gist**: build an app that allows studios to admins to add upcoming events that the public can register to attend.

Whenever I register for yoga classes, I have to sign into a portal that lists all of the available classes and the ones I've registered for. I always think to myself that it'd make a fun, simple-ish project that could be of use. This is one of the few projects in _Projectbook_ that's sort of business-y. The data model and needs are clear and interesting to me, though.

Okay, yeah, I'd probably call this **EventBud**. I'm sorry, I can't think of better names.

## Mock-Ups

Here's what the UI could look like. Top row is the Admin view. Bottom is the public attendee view.

![EventBud mock-ups. First view: index of your upcoming created events, including heading, "Add event" button, list of events with title, date, number of attendees and "View" button, plus a "View Past Events" link. Second view: "Add Event" form with heading and fields for name, description, datetime and location, plus a "Create Event" button. Third view: public upcoming events, much like the first view but without the "Add Event" button or past events link. Fourth view: event view, including the title, host, date, description and register button](./img/eventbud.webp)

## Specs

- Admins can sign up
- Admins can create upcoming events
    - Title
    - Description
- Public users (attendees) can register for events that haven't happened yet
- Admins can see the list of registered users

## Concepts

- Authentication
- Authorization
- Public registration
- Scheduling logic
- Dealing with time and timezones

## Extra Credit

- Student sign up to keep track of their events
- Allow Admins limit the number of attendees and prevent registration when limit is reached
- Accept payment when registering
- Make event details more rich with photo upload support and descriptions with a better editor (or Markdown)
- Email attendees before an event as a reminder

## References

- [Meetup](https://www.meetup.com)
- [Eventbrite](https://www.eventbrite.com)
