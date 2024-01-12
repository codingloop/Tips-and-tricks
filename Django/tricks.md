#### Generate secret key
```
from django.core.management.utils import get_random_secret_key
get_random_secret_key()
```


#### Inspecting Django DB Queries and connection
```
from django.db import connection as conn
from django.db import reset_queries as rq

# Prints the list of queries executed on DB
print(conn.queries)

# Resets connection.queries to empty list
rq()
```
