## Last Week's Accomplishments

I continued work on adding timouts to the test running.
Making this work with the perf-based test running will require a significant amount of work.
In order to ensure that each worker thred is able to properly handle signals from its children,
a single 'waiter'/'watchdog' thread will be used to manage signal handliong for all threads.

## This Week's Plan

Continue working on implementation of 'watchdog' thread

## Anything Blocking?

## Notes


