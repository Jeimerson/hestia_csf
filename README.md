Aqui está o texto formatado em **Markdown**:

```markdown
# 1. How To Install HestiaCP Free Panel

```bash
wget https://raw.githubusercontent.com/hestiacp/hestiacp/release/install/hst-install.sh
bash hst-install.sh --force
```

**Ref**: [Hestia Control Panel](https://hestiacp.com)

> **CAUTION**: Check & understand the scripts before you proceed.

---

# 2. How To Install CSF into HestiaCP Web UI

CSF (ConfigServer Security & Firewall) is a commonly used firewall for Linux servers. It provides an easy-to-use interface for managing firewall rules and can help improve the security of your server.

Run the following command as the **ROOT** user from your Linux terminal.  
(*Tested with HestiaCP v1.7.3 & Ubuntu 20.x*)

```bash
rm hestia_csf_install.sh* | wget https://raw.githubusercontent.com/jeimerson/hestia_csf/master/hestia_csf_install.sh
```

The above command will perform the following actions:

1. Download the script from `vvcares-github` repository.
2. Check if there is an existing CSF installation in `/etc/csf/`.
    - If it exists, it will proceed to **Step #5**.
    - If it doesn't exist, it will install a fresh/new CSF firewall.
3. Automatically add the HestiaCP backend port into `CSF.CONF > TCP_IN`.
4. Create an additional folder called `csf folder` inside `/usr/local/hestia/web/list/`.
5. Add the CSF link button into your `HestiaCP panel > main admin dashboard only`.
6. Exit.

---

**Important Note**:  
CSF should not be your only line of defense for securing your server. You should also follow best practices for server security, such as:  
- Keeping your server software up-to-date.
- Using strong passwords.
- Limiting access to only necessary users and services.

---

**Credit**: [VV Cares Blog](https://vvcares.com/blog/how-to-install-csf-on-hestia-cp-config-firewall/)
```
