## Last Week's Accomplishments

I continued working on statically linking B7 against DynamoRIO. Unfortunately,
it appears that making this work will require some modifications to DynamoRIO,
as it assumes the existance of an unzipped dynamorio directory.

I also setup SSH access to Travis vms (via ngrok), and confirmed that
they lack the necessary performance counters for using perf-based
instrumentation.

## This Week's Plan

I plan to investigate what changes would be necessary to DynamoRIO
to enable static linking. If it appears feasible, I might try to upstream
these changes at some point

## Anything Blocking?

## Notes


