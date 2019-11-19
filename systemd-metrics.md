# systremd collect 

# Add systemd collect options  add the option --collector.systemd

```
node_exporter-0.18.1.linux-amd64/node_exporter --collector.systemd
```

* It add # TYPE node_systemd_.+ queries

# Queries

* node_systemd_unit_state{name=~"postfix.+service"}
* node_systemd_unit_state{name=~"postfix.+service",state="active"}
