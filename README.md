# Ansible


    2  sudo apt update 
    3  sudo apt install ansible
    
    15 ssh-keygen
    16 ssh-copy-id ubuntu@172.31.36.98
    17 sudo passwd ubuntu

    18 sudo vi /etc/ssh/sshd_config.d/*.conf
                    PasswordAuthentication no  --->  change this to ---> PasswordAuthentication yes

    19  systemctl restart ssh
    4   sudo passwd ubuntu

    6  sudo mkdir -p /etc/ansile/      --> create ansible directory 
    7  vi /etc/ansile/hosts            -->  create hosts file and add the hostsnames or ips and thier password or 
    8  sudo vi /etc/ansile/hosts
        host file
                localhost
                [dev]
                172.31.34.185 ansible_user=ubuntu ansible_password=12345
                [test]
                172.31.35.191



    9  ansible ping
   10  ansible all -m ping
   11  ansible localhost -m ping
   12  ansible localhost -m yum -a "name=mginx state=present"
   13  ansible localhost -m apt -a "name=mginx state=present"
   14  ansible localhost -m apt -a "name=nginx state=present"

   

   20  ssh-copy-id ubuntu@172.31.36.98
   21  ansible localhost -m apt -a "name=nginx state=present"
   22  ansible localhost -b -m apt -a "name=nginx state=present"