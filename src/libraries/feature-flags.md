# Feature Flag Lib

**The gist**: build a library that allows code to be run only if a given resource has access to it. Users should be able to be opted into a feature, either by their own volition or based on certain conditions being true.

Working on non-trivial projects with a team means parallel work streams. Combine that with building functionality that's not ready for everyone yet, and it can get messy managing what functionality is available and what isn't. That's where feature flags come in. They let developers hide functionality behind a gate until it's ready to be launched, thus allowing code to be merged in and shipped without impacting the user until they want it to.

Feature flags enable incremental rollout too. So instead of launching a new feature all at once in a big bang release, you can steadily roll it out and monitor to see how it's going, fix any bugs before they come up, and launch to your entire userbase with more confidence.

Introducing and using feature flags was one of the most significant changes to my workflow throughout my entire career. It's also a pretty small and interesting library to build.

## Mock-Up

Here's what basic feature flag code in TypeScript could look like:

``` typescript
type FeatureFlag = (...args) => boolean;

// an existing feature visible to everyone
const canUseOldFeature:FeatureFlag = () => true;

if (canUseOldFeature())
  console.log("old feature visible for all")

interface User {
  email: string;
  favoriteSnack?: string;
}
const canUseSnackFeature:FeatureFlag = (user: User):boolean => {
  if (user.favoriteSnack) return true;
  else return false;
};

const snacky:User = {
  email: "snacky@example.com",
  favoriteSnack: "apples",
}
const sleepy:User = {
  email: "sleepy@example.com",
}

console.log("snacky can use Snack Feature?", canUseSnackFeature(snacky));
console.log("sleepy can use Snack Feature?", canUseSnackFeature(sleepy));
```

When you run that program, it outputs this:

```
old feature visible for all
snacky can use Snack Feature? true
sleepy can use Snack Feature? false
```

That mock-up makes use of a TypeScript type for defining feature flag functions, but it's not hard to imagine needing something a bit more complex that uses classes to implement functions.

## Specs

- Ability to define features and the logic that must be true to have it be available; usually just a method that returns a boolean that can be checked throughout the code
- Use the feature flag within code to hide or make features available

## Extra Credit

- Define an API to make it easy to opt a user into a given feature
- Support storing feature access in the database and loading from there

## See Also

- [Authorization Lib](./authorization-lib.md) — similar concepts but a slightly different application
