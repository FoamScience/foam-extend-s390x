# foam-extend-s390x
An unofficial version of Foam-Extend 4.0 built on IBM's s390x achitectures skipping some unimportant libraries and solvers 
from a reservoir engineer's point of view

The file `changes.patch` reflects the changes made to the official Git repository (at some point in the commit history) 
in order to compile the thing successfully
on IBM's s390x machines running Red Hat Enterprise Linux Server 7.4. Only libraries, solvers and utilities that might be useful
for reservoir engineers are retained! So, this is NOT COMPLETE. But, You can always compile the remaining libraries 
on your own!

>This version is for the "**Basics of Reservoir Simulation with OpenFOAM**" Course and nothing more! It was made for 
>learning, not for production; you have beed warned!

Also, ParaView is not compiled because I recommend using this installation only on IBM's LinuxOne Community servers. 
Post-processing is meant to be performed with `functionObjects` and `foamToVTK` if necessary

If you want to compile a more (complete and/or) recent version, you can clone the latest code from the official master branch
and:
```
git am -3 changes.patch
```
to apply the patch to the installation before attemting it. Then, you can build with `Allwmake.firstInstall` as usual.
