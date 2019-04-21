## Last Week's Accomplishments

I continued working on the caching implementation, and began work on a way
to cleanly shut down B7. Currently, the process is killed when using 'Ctrl-C'.
My plan is to add a SIGINT handler which waits for the current target processes to exit,
and then serializers the current state of all generator to a file.

## This Week's Plan

Fully implement ctrl-c handling. Also, investigate the mysterious segfaults
that occur with Dynamorio's on Luke's server. It's not clear whether B7 is at fault,
but we should try to handle this kind of situtation more gracefully (e.g. detect segfaults instead of
treating them as timeouts)

## Anything Blocking?

## Notes


