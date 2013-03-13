simple-stack
============

production-ready OpenStack with minimal fuss.

### Usage

1. install ubuntu quantal on your machines.

2. clone this repo: `git clone git@github.com:simple-stack/simple-stack.git`

3. define your environment:

```bash
cp envs/localhost.json envs/my_env.json
vi envs/my_env.json
# add your ips, passwords, subnets, etc.
```

4. run this on the controller (db/*-api/rabbit) node:

```bash
bin/install-controller envs/my_env.json
```

5. run this on N compute nodes:

```bash
bin/install-compute envs/my_env.json
```

and openstack lived happily ever after.

### troubleshooting

break into a screen session which tails most of the important logs:
```bash
bin/logs
```

