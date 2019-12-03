<h1>SRE_Challenge</h1>

<h2>Requirements</h2>
For this project, please think about how you would architect a scalable and secure static web application in AWS or another IaaS provider.

* Create and deploy a running instance of a web server using a configuration management tool of your choice. The web server should serve one page with the following content. 

```
<html>
<head>
<title>Hello World</title>
</head>
<body>
<h1>Hello World!</h1>
</body>
</html>
```

* Secure this application and host such that only appropriate ports are publicly exposed and any http requests are redirected to https. This should be automated using a configuration management tool of your choice and you should feel free to use a self-signed certificate for the web server.
* Develop and apply automated tests to validate the correctness of the server configuration.
* Express everything in code.
* Provide your code in a Git repository named SREChallenge on GitHub.com
* Be prepared to walk though your code, discuss your thought process, and talk through how you might monitor and scale this application. You should also be able to demo a running instance of the host.

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
