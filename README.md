## Ansiblefest 2020 - Chocolatey and Ansible

The resources for the talk are below:

* [Slides](https://github.com/pauby/ansiblefest2020/raw/master/Chocolatey.AnsibleFest.2020.Slides.pdf);
* Video (to be added later);

### Things To Know

* If you want to just play around with [Ansible](https://ansible.com) and [Chocolatey](https://chocolatey.org/products) you don't need a license or Chocolatey's [Quick Deployment Environment](https://chocolatey.org/docs/quick-deployment-environment);
* The `inventory` file in the `provision-env` folder is for installing tower and is not an Ansible inventory file;
* The `inventory.yml` file is a normal Ansible inventory you need to update before using (see the file);
* You'll need a [Chocolatey For Business License](https://chocolatey.org/products#chocolatey-for-business) `chocolatey.license.xml` placed in the `provision-env` folder to use Chocolatey's [Quick Deployment Environment](https://chocolatey.org/docs/quick-deployment-environment);
* To use Tower you also need a license;
* The `provision-env` folder contains the playbooks and files to create the demo environment;

### Create the environment

The demo environment was created in Azure and the `provision_demo_env.yml` file is used to do this. Look at `provision_vars.yml` for the variables used for the Azure provisioning and change them as necessary.

If you are going to use Chocolatey's [Quick Deployment Environment](https://chocolatey.org/docs/quick-deployment-environment) then there is a little more work to be done (see the comments in the file).

To provision one or more windows clients you need to run the `create_win_client_instance.yml` playbook. If you are using Chocolatey's Quick Deployment Environment, you should run `provision_qde_client.yml` on each Windows client.

The `configure_chocolatey_business.yml` playbook will configure your Chocolatey For Business clients to use the Quick Deployment Environment (QDE) server as a package source. If you are not using QDE then you will need to amend this playbook.

### Problems?

If you come across any problems then please raise an issue as normal. If you find yourself fixing an issue then please raise a pull request.

### Finally

We haven't covered every aspect of the demo here. See the video for more information (we will provide a link when / if it's released).