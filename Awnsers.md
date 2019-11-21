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

It works, if both have the same priority, but if one of them has a higher priority, the program could "fail".

For example: Process 0 checks 8 times while Process 1 checks only 1 time.

=> Proces 0 checks 8 times "while (turn != 0) ;" until Process one checks "while (turn != 1) ;"
=> Process 0 and Process 1 iterate the Prgram once, thatś ok for Process one, but Process 0 can´t interate the other 7 times because process one can´t call the "turn command" and without that command process 0 can´t iterate;
