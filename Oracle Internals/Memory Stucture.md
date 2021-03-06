# Memory Structure:  
Basically all the databases servers needs its own memory from the underlying servers. In oracle the memory allocation is divided into two parts.  
 * System Global Area or Shared Global Area 
 * Process Global Area or Program Global Area 

## System Global Area: 

The System Global Area (SGA) is a group of shared memory areas that are dedicated to an Oracle instance.  You only need to define two parameters (sga_target and sga_max_size) to configure your SGA, this will automatically allocate the memory for each component of SGA using a feature called Automatic Memory Management (AMM). SGA includes the below divisions.  

* Data buffer cache - cache data and index blocks for faster access. 
* Shared pool - cache parsed SQL(Save SQL query results) and PL/SQL(Functions results with same parameters) statements. 
* Dictionary Cache - information about data dictionary objects. 
* Redo Log Buffer - committed transactions that are not yet written to the redo log files. 
* JAVA pool - caching parsed Java programs. 
* Streams pool - cache Oracle Streams objects. 
* Large pool - used for huge memory consuming operations like backups, UGAs, etc.  

## Process Global Area: 
 
A memory buffer that contains data and control information for a server process. The information in a PGA depends on the Oracle configuration. 

> **Note:**
SGA is allocate when server startup and PGA will allocate when a Server process is started.


![](https://github.com/SqlAdmin/Oracle_CheatSheet/blob/master/Images/Oracle_CheatSheet_SGA%20and%20PGA.png?raw=true|alt=SGA and PGA)

## Reference:

[Reference Video](https://www.youtube.com/watch?v=zCKWRKSGlA0&t=2s)
