##Cloudify Package Installer Example

This blueprint demonstrates the use of the [Cloudify Package Installer Plugin] (https://github.com/kemiz/cloudify-package-installer-plugin) which allows you to install a given list of packages on a provisioned host.

### Usage

The plugin takes in 2 parameters, `package_list` & `install_from_repo`. For this example we are using a list of packages from a repository, we are installing on an Ubuntu host and our inputs are as follows:
	
	{
  		"image": "55aa4df7-1996-4507-955f-30f72d970836",
  		"package_list": ["openjdk-7-jdk", "lamp-server^", "tomcat7"],
  		"install_from_repo": true,
 		"flavor": 102,
  		"agent_user": "ubuntu"
	}

This example will install **Java OpenJDK 7**, **LAMP server Stack** & **Tomcat 7**

### Steps

Follow the standard steps to bootstrap a new manager and then:

- Upload blueprint
- Create Deployment
- Execute Install Workflow