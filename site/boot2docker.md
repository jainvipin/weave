---
title: Installing Weave with Boot2Docker
layout: default
---

## Installation with Boot2Docker

If you are running Docker inside the Boot2Docker VM, e.g. because you
are on a Mac, then the following changes are required to these
instructions:

Assuming you have fetched the 'weave' script via curl or similar, and
it is in the current directory, transfer it to the Boot2Docker VM and
make it executable like this:

    host1$ boot2docker ssh "cat > weave" < weave
    host1$ boot2docker ssh "chmod a+x weave"

Then, if we were trying to create the same containers as in the first
example above, the 'launch' command would be run like this:

    host1$ boot2docker ssh "sudo ./weave launch"

and the 'run' command like this:

    host1# C=$(boot2docker ssh "sudo ./weave run 10.0.1.1/24 -t -i ubuntu")
