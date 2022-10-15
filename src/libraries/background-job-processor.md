# Background Job Processor

**The gist**: build a library that allows clients to define jobs that get processed on an asynchronous queue separate from their application.

A really common need in an application is to offload long processing tasks to a background job queue. The job queue could be for something like sending an email where it doesn't need to happen immediately. Or it could be for processing something really important, like an order, that needs to call out to a variety of APIs and has many side effects. Maybe a large export file needs to be generated.

Whatever the need is, background job processors are critical to building back-end applications.

Don't expect to make something in a few hours that's stable and ready for the limelight. As always with these projects, this is for learning!

## Spec

This project is fairly complex, as you'll have to:

- Define the libraries API for building jobs
- Keep track of the jobs in the queue
- Process the jobs in queue
- Manage their state
- Have some way for checking in on which jobs have been completed, which are waiting, and which failed

## Examples

- [Sidekiq](https://github.com/mperham/sidekiq) — solid background processor for Ruby backed by Redis
- [Bull](https://github.com/OptimalBits/bull/) — background job processor for Node backed by Redis
- [Celery](https://docs.celeryq.dev/en/stable/getting-started/introduction.html) — Python background processor
- [work](https://github.com/gocraft/work) — Go background processor
