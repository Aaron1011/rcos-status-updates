## Last Week's Accomplishments

I discovered the issue with signal handling - SIGCHLD was not
being blocked on the main thread. With this issue fixed, I was able
to fully implement timeout support for both the 'perf' and 'dynamorio' backends

## This Week's Plan

Clean up and refactor some of the timeout code. There are still
some leftover fields/methods from my previous unsuccessful attempts

## Anything Blocking?

## Notes


