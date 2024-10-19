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

No! Not yet! Try JitPack if you must!

# License

[The Apache License 2.0](LICENSE), the same as libGDX.