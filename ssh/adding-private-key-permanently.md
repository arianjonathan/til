# Adding Private Key Permanently

`ssh-add ~/.ssh/<key>` is used to add and remember your passphrase, but for a more permanent solution you can edit `~/.ssh/config` file :

```bash
IdentityFile ~/.ssh/gitHubKey
IdentityFile ~/.ssh/id_rsa_buhlServer 
```
For all users on the computer to use the key put these lines into `/etc/ssh/ssh_config` and the key in a folder accessible to all.

To set the key specific to one host, you can do the following in your `~/.ssh/config` :
```bash
Host github
    HostName github.com
    User git
    IdentityFile ~/.ssh/githubKey
```

clone with @github instead of @github.com, and only this key will be tried. 

From [StackOverflow] (http://stackoverflow.com/questions/3466626/add-private-key-permanently-with-ssh-add-on-ubuntu)