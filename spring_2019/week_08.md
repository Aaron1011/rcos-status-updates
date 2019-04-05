## Last Week's Accomplishments

I extended the dynamorio backend to support testing both 32-bit and 64-bit
binaries. Unfortunately, this required building two separate copies of Dynamorio
 - one for 32-bit and one for 64 bit. Unless the dynamorio upstream repository
changes to support a 'hybrid' 32-bit and 64-bit 'drrun', this is the only
way to test both 32-bit and 64-bit binaries from a single 'b7' binary.

## This Week's Plan

Work on some additional post-merge cleanup for the signal handling code.
It may be possible to simply things further, now that we have a working
baseline merged into master.

## Anything Blocking?

## Notes


