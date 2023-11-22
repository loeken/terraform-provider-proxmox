i forked Telmet's provider to apply a simple fix in the casting of memory, turns out that whats in master is unstable, i dont see a point in reverting to older versions and publishing that or attempting to fix it. i ll archive this repo leave that published version up in terraform's registry

you can use it but if you add the disk {} block you ll end up with a broken kvm as it adds a new virtual disk  instead of replcaing the existing, you can creat the vm with vm_state stopped, use qm resize and start but this is more hacky then its worth i ll be moving on to:

https://registry.terraform.io/providers/bpg/proxmox/latest/docs/resources/virtual_environment_vm



note: if you do want to fix Telmet go and fork it from there, there is a github action included that does the publishing part
