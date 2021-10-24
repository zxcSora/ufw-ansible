
Role Variables Defaults/main.yml
------------
     ufw_default_incoming_policy: deny
     ufw_default_outgoing_policy: allow
     reset_rules: 'yes'
     
     
     ufw_rules:
       - rule: allow
         to_port: 22
         from_ip: 192.168.135.XXX
     ufw_ports_from_monitoring:
         - 9100
         - 9419
         - 15672
         - 5672
     ufw_ports_from_vpn:
         - 22
         - 5672

Using with inventory file example
--------------

     [BACKUP]
     bacula-backup
     
     [MONITORING]
     prod-mon