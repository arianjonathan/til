# Delete File by reference file time

find is a bit limited in terms of times you can reference against, it will search specific days, hours. If you want to delete files before/after a certain time, using a reference file is the way to go:

1. touch with timestamp
1. use find . older filename ls && rm 

```
touch -t 201906151600 ref; 
find /opt/services/edf/clientfiles/20006433/content/. -type f ! -newer ref -exec ls -l {} \;
find /opt/services/edf/clientfiles/20006433/content/. -type f ! -newer ref -exec rm {} \;
```
alternative: 
```
touch -t 201906151600 ref; 
find /opt/services/edf/clientfiles/20006433/content/. -type f ! -newer ref -ls -delete
```

If looking for files newer than reference file, just remove the "!".