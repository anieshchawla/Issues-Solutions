# gdb-issues
For MAC users:
if gdb gives the following issue:
```
Unable to find Mach task port for process-id 55644: (os/kern) failure (0x5).
 (please check gdb is codesigned - see taskgated(8))
 ```
 It means that it is not codesigned - easiest solution is run with command 'sudu'
 
 ```
 sudo gdb <name of binary>
 ```
 
 If still you get error like the following. Which I am getting for new edition of OSX.
 ```
 Starting program: <name of binary> 
During startup program terminated with signal ?, Unknown signal.
```

add file .gdbinit in the folder that you are working with and in that file add:
```
set startup-with-shell off
```
