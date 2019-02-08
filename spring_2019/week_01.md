## Last Week's Accomplishments

Last week, I worked on statically linking against DynamoRIO,
I was able to sucessfully compile DynamoRIO from the project rust buildscript (build.rs),
and compile against its api through bindgen.

At the moment, I have a sub-crate called dynamorio-sys, which handles interfacing with the DynamoRIO api.
It's able to build a binary statically linked against DynamoRIO, and execute the beginning of the inject sequence.

## This Week's Plan

I plan to get the DynamoRIO inject fully working.
The dynamorio-sys crate should be able to build a statically linked binary
which executes a target binary under DynamoRIO (wth the inscount client registered).
This might require some modifications to DynamoRIO itself, since it doesn't appear
to be set up properly for a fully statically-linked binary

## Anything Blocking?

DynamorIO currently has an open issue for static linking support:
https://github.com/DynamoRIO/dynamorio/issues/975

However, what exactly they mean by 'static linking' isn't clear.
All of the API samples for static linking show a process instrumenting *itself*,
not exec()ing a target binary. Having a fully self-contained binary might be tricky.

## Notes

It might be necessary to 'bundle' DynamoRIO's LD_PRELOAD
shared library - e.g. include the actual binary as a constant,
then write it out to a file
