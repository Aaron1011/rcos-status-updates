### Last Week's Accomplishments

Sandbox classloader architecture is mostly finalized and implemented.
The samebox classloader re-defines all classes, with a few exceptions (built-in Java classes,
and the special RunnerEvents class).

We can *begin* to start up a second game instance, but it ends up segfaulting Xorg due to the native library
hacks I'm doing.


### This Week's Plan

1. Stop Xorg from segfaulting (it's kind of annoying)
2. Determine if any changes need to be made to the classloader setup. In particular - how can we run multiple LWJGL displays in a single JVM instance?
3. Flesh out test API around starting new client.
4, Perform clean shutdown of secondary clients when tests end.


### Anything Blocking?

Native library/LWJGL issues might make it very annoying to have two phyiscal windows open from the same process.
