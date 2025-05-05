# Proxy Testing

Test proxy setup for Git proxying. Can it be broken, could you push, what else could be leaked?

# Setup

The proxy is setup to proxy github.com and chromium.googlesource.com. Any repos on those servers *should* be available.

# Usage

You shoud be able to clone any repo on these servers by cloning from https://git.domain.name and adding the host + path to the URL as shown below.

```bash
$ git clone https://git.domain.name/github.com/github/gitignore
Cloning into 'gitignore'...
remote: Enumerating objects: 10289, done.
remote: Total 10289 (delta 0), reused 0 (delta 0), pack-reused 10289 (from 1)
Receiving objects: 100% (10289/10289), 2.50 MiB | 3.27 MiB/s, done.
Resolving deltas: 100% (5601/5601), done.

$ git clone https://git.domain.name/chromium.googlesource.com/external/github.com/golang/protobuf
Cloning into 'protobuf'...
remote: Total 7304 (delta 4537), reused 7304 (delta 4537)
Receiving objects: 100% (7304/7304), 8.97 MiB | 3.22 MiB/s, done.
Resolving deltas: 100% (4537/4537), done.
```
