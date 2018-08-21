mauck
=====

Copyright 2018 Jason Burrell.

Demonstrate how to replace Fedora's mock with a simple Docker container.

To use, create an ephemeral container with:

```bash
docker run --rm --name maucktest_take1 --volume /tmp/blah/:/working:Z --volume /tmp/results:/results:Z jaybeeunix/mauck:latest /working/dash-0.5.9-5.fc28.src.rpm
```

...where `/tmp/{results,working}` are locations the container user can write to
and the SRPM is in `/tmp/working`. The resulting RPMs will be in `/tmp/results`.

