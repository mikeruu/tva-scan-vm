# tva-scan-vm
Heat template to create the TVA Scan VM

openstack stack create -e tva_env.yaml -t tva_vm.template tva-stack

The delete policy on the resources is set to retain so the stack can be deleted after its resources have been created.
We want to delete the stack to prevent the accidental replacement of the VM during a stack update, since it would loose the work done by TVA.
