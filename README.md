#Prereq
### VM - WMware pro workstation or Oracle Virtual box
### Gitbash


### 1.Open Ubuntu VM and install JAVA (make sure Java 8 is the default as the current version does not support Java 10 )
```sudo apt update``` 
```sudo apt-get install openjdk-8-jdk ```
###2.Import the GPG keys of the Jenkins repository using the following ```wget``` command:

```wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -``` 
### 2.The command above should output ```OK``` which means that the key has been successfully imported and packages from this repository will be considered trusted.

Next, add the Jenkins repository to the system with:
```sudo sh -c 'echo  deb https://pkg.jenkins.io/debian binary/ > /etc/apt/sources.list.d/jenkins.list'```

### 3.Install Jenkins.

Once the Jenkins repository is enabled, update the apt package list and install the latest version of Jenkins by typing:

```sudo apt update```
```sudo apt install jenkins```


### 4. Jenkins service will automatically start after the installation process is complete. You can verify it by printing the service status:

```sudo systemctl status jenkins```
You should see something similar to this:

```jenkins.service - LSB: Start Jenkins at boot time
Loaded: loaded (/etc/init.d/jenkins; generated)
Active: active (exited) since Wed 2018-08-22 13:03:08 PDT; 2min 16s ago
    Docs: man:systemd-sysv-generator(8)
    Tasks: 0 (limit: 2319)
CGroup: /system.slice/jenkins.service```