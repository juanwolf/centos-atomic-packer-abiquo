# centos-atomic-packer-abiquo
Abiquo templates for CentOS Atomic

## How to use it

### Setup an app in your Abiquo account

On your profile, if you click on your picture, you can see `manage applications`, click there and create a new one, you will receive a secret and a key that you can use in the next section.

### Modify the variables

You need to provide only 4 values before to have the atomic host template in your abiquo DC.
* abiquo_url: Will be the url of your abiquo server suffixed by /api. Example: https://portal.cloud.claranet.com/api
* abiquo_key: See above
* abiquo_secret: See previous section
* abiquo_datacenter: Virtual datacenter where to push this template.

### Run it

```
packer build ./centos-atomic-x86_64.json
```

## Configuration

All the installation is made via kickstart. You can modify it at your glance for anything, changing root password, default user, etc...

I invite you to have a look at the redhat documentation about the [kickstart syntax](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/installation_guide/sect-kickstart-syntax). You can even use ansible to provision your atomic host using the [ansible provisioner](https://www.packer.io/docs/provisioners/ansible-local.html).

## Contribution
Every contribution is more than welcome, you can add more security around this template or provide new ones, such as fedora, or coreos. :smile:


