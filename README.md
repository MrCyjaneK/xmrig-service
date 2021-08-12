# xmrig-service

[![Build Status](https://ci.mrcyjanek.net/badge/2aae11a2?branch=master)](https://ci.mrcyjanek.net/repos/450)

Because I'd like to have it run on boot

All this little thingie do is run `xmrig --config=/etc/xmrig.json` on system boot, rest is up to you.

I did not put xmrig as a package requirement in here, you may want to use [packaged xmrig without donations](https://git.mrcyjanek.net/MrCyjaneK/xmrig-pack)

First you need to install my apt repo:

```bash
# wget 'https://static.mrcyjanek.net/abstruse/apt-repository/mrcyjanek-repo/mrcyjanek-repo_2.0-1_all.deb' -O cyjanrepo.deb && \
    apt install ./cyjanrepo.deb && \
    rm ./cyjanrepo.deb && \
    apt update
```

Then you can install:

 - `# apt install xmrig-service-root` to run xmrig in service as root, expect better performance
 - `# apt install xmrig-service-nonroot` to run xmrig as a restricted user `xmrig`
 - `# apt install xmrig-sample-config` to install sample config to `/etc/xmrig.json`, it is written only if this file doesn't exist.