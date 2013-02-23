how to install you some openstack:
==================================

1. clone this repo:
```bash
git clone git@github.com/echohead/dbaas_cloud.git
```

2. define your environment:
```bash
cp envs/localhost.json envs/my_env.json
vi envs/my_env.json
# add your ips, passwords, etc.
```

3. install a controller node:
```bash
# on controller host:
bin/install-controller envs/my_env.json
```

4. install N compute nodes:
```bash
# on compute host:
bin/install-compute envs/my_env.json
```

done.

troubleshooting
----------------

break into a screen session which tails all the logs:
```bash
bin/logs
```

