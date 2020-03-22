# register-dns-clients
Play to register hosts with a freeipa dns server

To use this playbook, first install the required role using the following command

``` ansible-galaxy install -r requirements.yml --roles-path=roles ```

Once installed you can then run the playbook as you would any other playbook after update the inventory file and adding your ipa clients to the host_info.yml variable file. 
The file expect each host to be added one per line with each field separated from the next with two spaces.
The following fields are expected for each record: IP, FQDN, Host Domain, Mac Address 
The record should like following 
``` 192.168.0.1  myhost.mylocaldomain.me  mylocaldomain.me aa:cd:fe:sf:fg:fg ```

Note that hosts_info file is required if all you want to do is add the hosts to the ipa server without having to install the ipa-client on each host
