# spritz
Fixing your SpriteBatch on GWT since day 3.

# What happened?

SpriteBatch broke in 1.13.0 on GWT! Things ranging from ScrollPane to TextField simply won't draw,
and throw many OpenGL Errors (which are usually really just warnings). As a stop-gap measure, I'm
making this repo so users who target GWT can depend on a fixed SpriteBatch without waiting for another
release.

Oh, and I'm making everything that's private or package-private in SpriteBatch public or protected, and
using **THE POWER OF THE WRITTEN WORD**, that is, ***DOCUMENTATION***, to indicate if a field is not
intended to be used. If you need to use something in a subclass, you just *can*. It's about time.

# Get it!

The dependency for a libGDX project's core module looks like:

```groovy
implementation "com.github.tommyettinger:spritz:0.0.1"
```

This assumes you already depend on libGDX; spritz depends on version 1.13.0 or higher. This does depend on Java 8 as a
language level, but it uses no APIs added in Java 8 (making it safe to use on the antiquated RoboVM stable version).
Targeting 8 instead of 7 means you can actually build this with recent JDKs, such as Java 21, which have dropped support
for the teenage (mutant) Java 7 target.

If you use GWT, this is compatible. It needs this dependency in the html module:

```groovy
implementation "com.github.tommyettinger:spritz:0.0.1:sources"
```

And this in GdxDefinition.gwt.xml :

```xml
<inherits name="com.github.tommyettinger.spritz" />
```


# License

[The Apache License 2.0](LICENSE), the same as libGDX.