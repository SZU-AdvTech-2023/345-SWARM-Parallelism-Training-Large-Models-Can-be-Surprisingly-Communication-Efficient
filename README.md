# Tips

This folder contains the scripts that are necessary to launch large-scale language modeling experiments using SWARM Parallelism. The official link is:https://github.com/yandex-research/swarm/tree/main/swarm.

## To reproduce

1. On a dedicated stable (yet possibly low-performance) server, install the code with `pipeline/setup.py` and
   run `python start_monitor.py`,which will generate a initial peer meanwhile;
2. Run `setup_and_launch_server.sh` on GPU-enabled servers,
   replacing the '{init_peer}' in the shell with the value given by step 1;
3. Run `setup_and_launch_trainer.sh` on CPU-only nodes, also adjusting `'{init_peer}'` to use the same libp2p ID as
   given by the step 1;
4. Some file path and dataset path have to be modified by yourself .
