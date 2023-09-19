#### Generate secret key
```
from django.core.management.utils import get_random_secret_key
get_random_secret_key()
```


#### Inspecting Django DB Queries and connection
```
from django.db import connection
from django.db import reset_queries

# Prints the list of queries executed on DB
print(connection.queries)

# Resets connection.queries to empty list
reset_queries()
```
