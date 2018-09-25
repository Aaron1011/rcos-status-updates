### Last Week's Accomplishments

Experimented with calling Kotlin coroutines from Java, and determined that it doesn't work.
Duplicating each 'suspend' function seeks to be the only way to have Kotlin and Java support

Decided on classloader approach - one class loader per client instance.
Determins that Mixin bugs are still blocking the switch to an obfuscated (production) SpongeForge jar


### This Week's Plan

Get a working version of the multi-classloader setup. We should be able to cleanly start and close two separate client
instances from a single java process.


### Anything Blocking?

Mixin runtime-deobfuscation bugs mean end users still need ForgeGradle.
