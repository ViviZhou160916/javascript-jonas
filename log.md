#### 1. git failed in cloning code
```bash
git config --global http.version HTTP/1.1
git config --global http.sslVerify false
git config --global http.lowSpeedLimit 0
git config --global http.lowSpeedTime 999999
git config --global http.postBuffer 1048576000
```

then try adding ssh key
```bash
ssh -T git@github.com  // to check whether ssh is working. it shows git@github.com: Permission denied (publickey).

ssh-add /Users/joy/Documents/configurations/ssh/id_ed25519 //add the ssh key, re-run above script, it shows "Hi ViviZhou160916! You've successfully authenticated, but GitHub does not provide shell access." Try clone the project, it works
```