# systremd collect 

# Add systemd collect options

* node_exporter-0.18.1.linux-amd64/node_exporter --collector.systemd

# Queries

* node_systemd_unit_state{name=~"postfix.+service"}
