#Extracting Specified Path to a Different Folder Location

It's pretty trivial to view/extract specific path within a tar.xz/tar.gz file
```bash
tar -xpvf /opt/nfs/shoppingLogs/ashdod/archive/pcs_201510090800_ashdod.tar.xz 201510090800/providerMessages/IHG/PROVIDER_RESERVE_SEARCH
```

Similarly it's pretty trivial and straightforward to extract a tar.xz/tar.gz to a different folder location
```bash
tar -xpvf /opt/nfs/shoppingLogs/ashdod/archive/pcs_201510090800_ashdod.tar.xz -C /home/support/testing
```
or
```bash
tar -xpvf /opt/nfs/shoppingLogs/ashdod/archive/pcs_201510090800_ashdod.tar.xz --directory=/home/support/testing 
```

How to do *both*?
Syntax as follows
```bash
tar -xpvf /path/to/tar/file.tar.xz -C /path/to/destination path/within/tar/file 
```
