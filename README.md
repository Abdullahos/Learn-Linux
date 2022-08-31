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

|  Adminstrative        | used by processes that provide supporting services    |Most users have regular user accounts which they use for their day-to-day work.         |   Have id of 0        |                                                       |Like system users, regular users have limited access to the system
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------         |  its name is root     | These processes, or daemons, usually do not need to   |
        |                       |  run as the superuser. They are assiged non-privileged|
        |                       | accounts that allow them to secure their files and    |
        |                       | other resources from each other and from regular users|
        |                       |  on the system.                                       |    
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------


## View User info
### of currenty logged in user
![image](https://user-images.githubusercontent.com/51336081/187587322-e0ee38e8-5582-4712-a0e7-736372f773ae.png)

### of specific user
![image](https://user-images.githubusercontent.com/51336081/187587398-c552ee26-c6bb-432f-9e35-ba7352b9292c.png)

## View Owner of a file
```
ls -la <filePath>
```
![image](https://user-images.githubusercontent.com/51336081/187587593-8dbdef5f-2fee-4c3b-8bff-709dfc9824df.png)

## View Owner of the current directory
ls -ld ..
![image](https://user-images.githubusercontent.com/51336081/187588013-faa54980-acbf-4b13-b0fa-ce75f781476a.png)

## Show proccess of the current user
```
ps -au
```
## Information about users
```
cat /etc/passwd
```
user: pass: uid: group_id: real name: home dir: default bash program 

## The same is for Groups
group is a collection of users that need to share access to files and other system resources.
Linux store them in a /etc/group
u can found it by:
```
cat /etc/group
```
## Gaining Superuser Access
**This unlimited privilege, however, comes with responsibility. The root user has unlimited power to
damage the system: remove files and directories, remove user accounts, add back doors, and so
on. If the root user's account is compromised, someone else would have administrative control of
the system. Throughout this course, administrators are encouraged to log in as a normal user and
escalate privileges to root only when needed.**

** By logging in as the superuser, the entire desktop environment unnecessarily runs
with administrative privileges. In that situation, any security vulnerability which would
normally only compromise the user account has the potential to compromise the
entire system. **

## To temporarily gain superuser privileges
use su, sudo, or PolicyKit

## Switching Users
The **su** command allows users to switch to a different user account
