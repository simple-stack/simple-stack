simple-stack
============

production-ready OpenStack with minimal fuss.

### Usage

- install ubuntu quantal on your machines.

- clone this repo: `git clone git@github.com:simple-stack/simple-stack.git`

- define your environment:

```bash
cp envs/localhost.json envs/my_env.json
vi envs/my_env.json
# add your ips, passwords, subnets, etc.
```

- run this on the controller (db/*-api/rabbit) host:

```bash
bin/install-controller envs/my_env.json
```

- run this on N compute nodes:
```bash
bin/install-compute envs/my_env.json
```

and openstack lived happily ever after.

troubleshooting
----------------

break into a screen session which tails most of the important logs:
```bash
bin/logs
```

