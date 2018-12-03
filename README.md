# redis-trib
支持群集节点指定auth参数使用

由于原版的针对已经配置auth的redis，无法使用此群集脚本，所以，特意修改一版支持指定auth参数的版。

Usage: redis-trib <command> <options> <arguments ...>

  create          host1:port1 ... hostN:portN
                  --replicas <arg>
                  --auth <arg>
  check           host:port
                  --auth <arg>
  info            host:port
                  --auth <arg>
  fix             host:port
                  --timeout <arg>
                  --auth <arg>
  reshard         host:port
                  --from <arg>
                  --to <arg>
                  --slots <arg>
                  --yes
                  --timeout <arg>
                  --pipeline <arg>
                  --auth <arg>
  rebalance       host:port
                  --weight <arg>
                  --auto-weights
                  --use-empty-masters
                  --timeout <arg>
                  --simulate
                  --pipeline <arg>
                  --threshold <arg>
                  --auth <arg>
  add-node        new_host:new_port existing_host:existing_port
                  --slave
                  --master-id <arg>
                  --auth <arg>
  del-node        host:port node_id
  set-timeout     host:port milliseconds
  call            host:port command arg arg .. arg
  import          host:port
                  --from <arg>
                  --copy
                  --replace
                  --auth <arg>
  help            (show this help)

For check, fix, reshard, del-node, set-timeout you can specify the host and port of any working node in the cluster.
