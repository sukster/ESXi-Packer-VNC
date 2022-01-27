# ESXi-Packer-VNC
A VIB file which will add a persistent firewall rule to VMWare ESXi so that Packer can connect to VNC. You may find this helpful if you want to setup DetectionLab on ESXi. Relates to prerequisite #5 here: https://github.com/clong/DetectionLab/blob/master/ESXi/README.md

This VIB automates the procedure of adding a firewall rule described in this article: https://nickcharlton.net/posts/using-packer-esxi-6.html. It was generated based on this article: https://www.altaro.com/vmware/how-to-create-persistent-firewall-rules-on-esxi/.

How to install:
1. Ensure that the Acceptance Level in ESXi is set to "Community" by going to Manage -> Security & Users -> Acceptance Level or running **esxcli software acceptance set --level=CommunitySupported**
2. Upload the VIB file to /tmp directory of the ESXi server
3. Login to ESXi via SSH and run: **esxcli software vib install -v /tmp/packer-vnc.vib -f**
4. Check that the VIB was installed successfully: **esxcli software vib list | grep 'packer'**
