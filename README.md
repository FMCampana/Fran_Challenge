<h1>Fran_Challenge</h1>


<h2>Resources Used</h2>

* Ansible
  - Automation tool that is used for configuration management, executing consistent server-side tasks, and web application deployments. This is "Infrastructure as Code".
  - Used Ansible modules to test server configuration & function, strategies used were based off of: http://docs.ansible.com/ansible/latest/test_strategies.html 
* Vagrant
  - Used to spin up scalable virtual machines that can be leveraged for producing consistent environments
  - Vagrant manages VirtualBox to create _n_ instances of the desired environment
  - VM Box OS - ubuntu/trusty64
    - OS source hosted by: [VagrantCloud](https://app.vagrantup.com/ubuntu/boxes/trusty64)
  - Specified requiring Vagrant version 1.7.0 (or above)

<h2>How to Run</h2>

1. Clone repo to your local machine
2. Once git clone has completed, navigate into the directory via Terminal
3. Download & Install required dependencies
    - https://www.virtualbox.org/wiki/Downloads
    - https://www.vagrantup.com/downloads.html
    - http://docs.ansible.com/ansible/latest/intro_installation.html
4. Once dependencies are installed, simply start up Vagrant and it will handle the rest
    - While in SRE_Challenge directory... run: `vagrant up`
5. Navigate to [192.168.50.4](https://192.168.50.4) in your browser of choice
    - Note: Will redirect to https, but is currently using a self-signed certificate
