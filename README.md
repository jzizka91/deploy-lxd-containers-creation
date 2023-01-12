# LXC Container Deployment 

This repository holds the deployment of LXC container with Ubuntu 20.04.

## Usage

1. Modify configuration:

    * Edit:
        * `config/01-netcfg.yaml.j2`
        * `config/temporary-pubkeys`
        * `vars/vars.yml`

2. Create a new LXC container:


    * `hosts` is the file that contains host(s) where container will be created.
    * `ipnum` is the last oktet of configurated LXD IP address pool.
    * `cname` is the container name.

    ```
    ansible-playbook -i hosts deploy.yml -e cname=<username> -e ipnum=<last_oktet> -e host=<lxd_host_ip>
    ```
