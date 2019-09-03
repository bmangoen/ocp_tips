# ocp_tips

```
 ansible nodes -i inventory/hosts.poc_acoss -m shell -a 'export no_proxy='10.0.0.0/8,.recouv'; export http_proxy=http://squid.cnp.recouv:8080/;export httpsp_proxy=http://squid.cnp.recouv:8080/; subscription-manager register --username {{ rhsm_user }} --password {{ rhsm_password }};' -e @/tmp/rhsm.yaml --ask-vault-pass
 ```
