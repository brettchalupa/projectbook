# Authorization Lib

**The gist**: build a library that allows developers to define permissions for a given action a user can take.

Authorization (whether or not a given user is able to take an action) is a major part of building any application with users, even more so if there are different permission levels. Since it's such a common need, it can be really helpful to have a library for a given framework or language to do so.

_Note_: authorization is different than authentication. Authentication is checking if a client/user is who they say they are. Authorization is about allowing access to specific actions.

## Spec

- Ability to define actions and their logic for access
- Convenient methods for checking access for a given action with a user
- Easy to unit test

## Concepts

- Logic
- Composition
- Library development

## Mock-Up

In plain Ruby, this could look something like:

``` ruby
class PostAuthorizer
  def initialize(user, post)
    @post = user
    @user = user
  end

  def show?
    true
  end

  def update?
    @post.organization.users.include?(@user)
  end
end
```

Then, within the code where you want to check, you'd call out with:

``` ruby
if PostAuthorizer.new(user, post).update?
  post.update!(params)
end
```

That's all well and good! It's just simple Ruby objects and easy to test. But it's not exactly the nicest API. The code for defining an authorizer could be simplified. Maybe there's a way to define multiple actions that are available to all or a default. Something like:

``` ruby
class PostAuthorizer
  public :show, :like
end
```

What if there was a simpler API for checking authorization, like:

``` ruby
authorized_to_update?(user, post)
authorized_to_read?(user, post)
authorized_to_like?(user, post)
```

What's possible for defining these sorts of APIs will vary based on languages, but these are just some off-the-cuff ideas. Whether you use inheritance or composition or functions is totally up to you.

## Examples

- [pundit](https://github.com/varvet/pundit) is a mature and nice Ruby authorization library
