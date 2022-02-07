# How to apply timezone to datetime 

below is an example of applying utc tz to d

```
from datetime import datetime, timezone

d = datetime.strptime("2022-02-21T14:19:42+04:00", "%Y-%m-%dT%H:%M:%S%z")
d.astimezone(timezone.utc) #  2022-02-21T10:19:42+00:00

```
