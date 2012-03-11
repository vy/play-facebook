# Introduction

play-facebook is a [Play Framework](http://www.playframework.org/) archetype providing basic Facebook authentication mechanics. It integrates Facebook Login into [Secure](http://www.playframework.org/documentation/1.0/secure) module infrastructure. Hence, if you are familiar with Secure module, you can directly bootstrap your own Facebook Login integrated application.

# Installation

1. Checkout the play-facebook sources and do `play deps`.
3. Edit `FBOAuth` variable in `app/controllers/Security.java` according to your Facebook Application credentials. ([Doesn't have one yet?](http://www.facebook.com/developers/createapp.php))
4. Do `play run`.

# Usage

You don't need any other extra configurations. Just start using `@With(Secure.class)` and/or `@Check("admin")` annotations within your controller classes.

As a side node, all login failures will be redirected to `Application.index()`. You can alter this behaviour by editing the `views/login.html`.
