how to install you some openstack:
==================================

#### Preface: in the beginning was quantal

```
see preface
```

#### Chapter 1: the repo is cloned
```bash
git clone git@github.com/echohead/dbaas_cloud.git
```

#### Chapter 2: an environment is born
```bash
cp envs/localhost.json envs/my_env.json
vi envs/my_env.json
# add your ips, passwords, etc.
```

#### Chapter 3: a node asumes control
```bash
# on controller host:
bin/install-controller envs/my_env.json
```

#### Chapter 4: rise of the machines
```bash
# on compute N hosts:
bin/install-compute envs/my_env.json
```

and openstack lived happily ever after.

troubleshooting
----------------

break into a screen session which tails all the logs:
```bash
bin/logs
```

