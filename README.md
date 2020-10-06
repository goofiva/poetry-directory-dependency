# poetry-directory-dependency

Replicating this error...

    cd /path/to/poetry-directory-dependency/package-a
    poetry install
    
When directory dependencies are a bit more complex than... 
    
    a -> b
    b -> c
 
Poetry fails to resolve all paths. In this example here, the dependency is as follows...
 
    a -> b
    a -> d
    b -> c
    d -> b
    