# ocp_tips

```
ansible nodes -i inventory/hosts.poc_acoss -m shell -a "export no_proxy=10.0.0.0/8,.recouv; export http_proxy=http://squid.cnp.recouv:8080/;export https_proxy=http://squid.cnp.recouv:8080/; subscription-manager remove --all; subscription-manager unregister; subscription-manager clean"
```

```
ansible nodes -i inventory/hosts.poc_acoss -m shell -a "export no_proxy=10.0.0.0/8,.recouv; export http_proxy=http://squid.cnp.recouv:8080/;export https_proxy=http://squid.cnp.recouv:8080/; subscription-manager register --username {{ rhsm_user }} --password {{ rhsm_password }}; subscription-manager refresh; subscription-manager attach --pool={{ rhsm_pool_id }}" -e @/tmp/rhsm.yaml --ask-vault-pass
 ```


