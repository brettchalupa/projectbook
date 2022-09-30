# Unit Testing Lib

**The gist**: write a library that runs unit tests for the language you're learning.

Writing automated tests that verify your code's correctness is important. So important that pretty much all modern languages have unit testing functionality built right in. But writing your own testing library is a great way to learn the language, as you'll have to understand how to build friendly APIs, compare types, scoping, and run the tests.

## Specs

- Define what the test syntax will look like for your library
- Add support for a basic equals comparison
- Write a test runner that executes the tests
  - If the tests pass, exit with a 0 status
  - If the tests fail, output what failed and exit with a non-zero status

## Extra Credit

- Add support for an includes comparison
- The sky's the limit with other comparisons

## Resources

- [Test Runner from Scratch](https://www.destroyallsoftware.com/screencasts/catalog/test-runner-from-scratch) — excellent screencast on doing this in Ruby
- [Jest](https://jestjs.io) — for JS/TS
- [minitest](https://github.com/minitest/minitest) — for Ruby
- [RSpec](http://rspec.info) — for Ruby
- [Ginkgo](https://github.com/onsi/ginkgo) — for Go
