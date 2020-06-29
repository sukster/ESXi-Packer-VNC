# ESXi-Packer-VNC
A VIB file which will add a persistent firewall rule to VMWare ESXi so that Packer can connect to VNC. You may find this helpful if you want to setup DetectionLab on ESXi. Relates to prerequisit #5 here: https://github.com/clong/DetectionLab/blob/master/ESXi/README.md

This VIB automates the procedure of adding a firewall rule described in this article: https://nickcharlton.net/posts/using-packer-esxi-6.html. The VIB was created based on this article: https://www.altaro.com/vmware/how-to-create-persistent-firewall-rules-on-esxi/.

The Acceptance Level in ESXi needs to be set to "Community".
