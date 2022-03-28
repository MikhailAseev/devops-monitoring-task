# DevOps monitoring with Prometheus, Prometheus Node Exporter and Grafana
## Task Description

Write a Vagrantfile which (after `vagrant up`):
- starts Ubuntu 20.04 VirtualBox virtual machine (generic/ubuntu2004);
- automatically installs Docker and Docker Compose packages inside the VM (using Ansible);
- installs Prometheus Node Exporter and starts it inside the VM (using Ansible);
- starts 2 containers using Docker Compose (Docker Compose is also hooked by Ansible):
    - the first container has running Prometheus which is set up to recieve metrics from the Node Exporter on the Ubuntu VM;
    - the second container contains a configured Grafana: as a datasource Prometheus run in the first container is specified, Node Exporter Full dashboard (ID 1860) is imported which visualizes metrics received from the Node Exporter.

Additional network requirements:
- the container with Grafana has to forward port 3000 to the Ubuntu VM;
- Ubuntu VM has to forward 3000 port to the host machine, so the user could open http://localhost:3000 inside the browser on his/her host machine and be able to see Grafana Dashboard with the metrics received from the Ubuntu VM.
