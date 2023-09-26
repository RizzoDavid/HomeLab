# Ansible
I already have ESXI as a Hypervisor and then Winodws Server installed on another system. To manage all of my future virtual machines, I am going to use ansible. That is the fist VM I am creating. Below are listed the spcecs: 
<ul>
 <li>2 vCPUs</li>
 <li>4 GB Ram</li>
 <li>25GB Hard Disk</li>
</ul>

After Installing Ubuntu and enabling ssh from my main computers with SSH keys, I ran updates with the following command.
    ```
    sudo apt update && sudo apt upgrade -y
    ```
Then a snapshot was created in VMWare ESXI as a restore point. Then Ansible was installed with PiP
    ```
    curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
    python3 get-pip.py --user
    python3 -m pip -V
    python3 -m pip install --user ansible
    ```
There was an error with the path mapping and I had to run this command to fix it
    ```
    cp .local/bin/ansible  /usr/local/bin
    ```
I need to create a ssh key for the ansible machine to ssh into the other devices. After than I need to setup the other VMs before I can configure ansible the rest of the way. 

# Docker VMWare
I am installing docker on Red Hat Enterprise 9 without a gui. I have configured a root password and a secondary administror user so that the root account is not being used. 

    ```
    4 vCPUs
    8 GB Ram
    40 GB Hard Disk
    ```
    
After the operating system is installed, I will then set up ssh using the key created on the ansible system. This will only allow ssh into the system via the ansible machine.  