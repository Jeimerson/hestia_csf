1. How To Install HestiaCP Free Panel:

wget https://raw.githubusercontent.com/hestiacp/hestiacp/release/install/hst-install.sh
bash hst-install.sh --force

Ref: Hestia Control Panel (hestiacp.com)

CAUTION: Check & understand the scripts before you proceed.
2. How To Install CSF into HestiaCP Web UI:

CSF (ConfigServer Security & Firewall) is a commonly used firewall for Linux servers. It provides an easy-to-use interface for managing firewall rules and can help improve the security of your server.

Just run this below command as ROOT user from your linux terminal. (Tested with HestiaCP v1.7.3 & Ubuntu 20.x)
``
rm hestia_csf_install.sh* | wget https://raw.githubusercontent.com/jeimerson/hestia_csf/master/hestia_csf_install.sh
``
The above command will do as below:

    Download the script from vvcares-github repo
    It will check if there is an existing CSF installation in ‘/etc/csf/’.
    If exists, it will proceed to Step#5
    If not exist, it will install fresh/new CSF firewall
    It will automatically add the hestiacp backend port into ‘CSF.CONF > TCP_IN’
    Create an additional folder called ‘csf folder’ inside ‘/usr/local/hestia/web/list/’
    Add the CSF link button into your ‘hestiacp panel > in main admin dashboard only’ & Exit.

It is important to note that CSF should not be your only line of defense for securing your server. You should also follow best practices for server security, such as keeping your server software up-to-date, using strong passwords, and limiting access to only necessary users and services.

Credit: https://vvcares.com/blog/how-to-install-csf-on-hestia-cp-config-firewall/
