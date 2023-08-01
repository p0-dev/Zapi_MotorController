a0m = a0 master (for master node)
a0s = a0 slave (for slave node)

as these are 2uC (two controllers system)

[VERSION INFORMATION]
v1 : original version from factory (Zapi)
+ zapi version: 0.60
	- cannot be set to nominal current of 150A (maximum at 100A)
	- cannot be monitored "motion torque NM"

v2 : update version for monitoring "Motion Torque NM"
+ zapi version: 0.63
	- can be able to set nominal current to 150A
	- can be able to monitored "motion torque NM"
	- known bugs: have the alarm code of "WAITING FOR NODE" on main node and "OUT MISMATCH20" on secondary node

v3: update version for fixing "WAITING FOR NODE" and "OUT MISMATCH20" problem
+ zapi version: 0.63
+ date: 01.08.2023