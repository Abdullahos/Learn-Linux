# Learn-Linux

# Users
A user account is used to provide security boundaries between different people and programs that
can run commands.

Identified by ID or UID

Every process (running program) on the
system runs as a particular user. Every file has a particular user as its owner

Users types:
super users, 
            System users,
                         Regular users
                         
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
        |         Super User    |                  System User                          | Regular User
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Role  |  Adminstrative        | used by processes that provide supporting services    |Most users have regular user accounts which they use for their day-to-day work.         |   Have id of 0                                                                |Like system users, regular users have limited access to the system
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------         |  its name is root     | These processes, or daemons, usually do not need to   |
        |                       |  run as the superuser. They are assiged non-privileged|
        |                       | accounts that allow them to secure their files and    |
        |                       | other resources from each other and from regular users|
        |                       |  on the system.                                       |    
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------
