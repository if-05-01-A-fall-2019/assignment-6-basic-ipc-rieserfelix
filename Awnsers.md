## 1. Race Condition 

The second process, overwrites the first process. For Example: You want to print two sheets but get only one, because one document is overwritten


## 2. Disabling Interrupts
### i: 
It works only on a single-core processor, because the scheduler could take two processes at the same time into the critical region on a multi-core maschine.

### ii:
Because you can crash the maschine. If you have just one core and you run an endessloop, you can´t stop it anymore.


## 3. Peterson's Solution
### i:
It works, but process 1 have to wait, till process 0 leaves and only than, process one can finish "enter_region()".

### ii:
