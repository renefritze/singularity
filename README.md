# Singularity + Vagrant Trial

The Vagrant box includes the newest singularity client and converts our pymor-demo docker image to the
Singularity Image Format on provisioning

## Quickstart

```
git clone https://github.com/renefritze/singularity && \
  cd singularity && \
  vagrant up && \
  vagrant ssh -- -t 'singularity exec pymor-demo.sif pymor-demo heat '
```

## Caveats

 - Not all demos work yet due to rendering setup issues.
 - You cannot run an singularity image inside the vagrant box from /vagrant. 
   There's a conflict between squashfs and overlayfs which seems hard to fix.
