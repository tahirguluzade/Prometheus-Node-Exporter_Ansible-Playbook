# Prometheus-Node-Exporter_Ansible-Playbook

- **In this ansible playbook we are gonna installing Prometheus and Node Exporter in our remote server.**
- [x] Do not forget to write ip address of your remote server to `inventory` file as weel as change `ansible_user` to username of your remote server where it will try to conncet via ssh.
- [x] You need to add public key where ansible is running to your remote server 
- [x] Playbook also adding Node Exporter to prometheus to integrate with it
- [x] After succesfully installation you can go your browser and type `<ip address of remote server>:9090` , because as a default prometheus running on port number `9090`. You can also check integration of Node Exporter in Prometheus by adding `<ip address of remote server>:9090/targets`.
- [x] To visit Node Exporter seperately add following to your browser `<ip address of remote server>:9100` (as a default it runs on port number `9100`)
- [x] If you are using firewall, then you need to open those ports:
```
sudo firewall-cmd --zone=public --add-port=9090/tcp 
sudo firewall-cmd --zone=public --add-port=9100/tcp
sudo firewall-cmd --reload
```
