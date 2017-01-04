**_Ansible playbook for 3 node (single master, two slaves) kubernetes cluster_**


**_Running the setup_**

    If inventory isn't being handled dynamically, cross check the values in the `staging` or `production` files

```
    # ansible-playbook -i staging kube.cluster.yml --list-tasks
    # ansible-playbook -s -i staging kube.cluster.yml
```

    To setup only the masters, run;
```
    # ansible-playbook -s -i staging kube.masters.yml
```
    To setup only the minions, run;
```
    # ansible-playbook -s -i staging kube.minions.yml
```

`### Close to the end :) ###`

### **Notes**:

 - Running ansible via bastion fails when the hosts aren't added to the known_hosts on the bastion box and the prompt isn't shown