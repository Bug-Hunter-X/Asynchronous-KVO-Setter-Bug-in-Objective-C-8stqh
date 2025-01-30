# Asynchronous KVO Setter Bug in Objective-C

This repository demonstrates a subtle bug that can occur in Objective-C when using Key-Value Observing (KVO) with custom setter methods that perform asynchronous operations.  The problem arises when the asynchronous operation completes *after* the observer's `observeValueForKeyPath:` method is called, potentially leading to stale data or crashes.

The `AsynchronousKVOBug.m` file contains the buggy code, while `AsynchronousKVOBugSolution.m` provides a corrected version.

## Reproducing the Bug

1. Clone this repository.
2. Compile and run the project (requires Xcode).  You should observe the bug which might manifest as incorrect data or a crash depending on timing and asynchronous completion.