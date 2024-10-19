# Changing file ownership
**Steps**
- When we perform the  'ls -l /flag' command, we realise that we can see that the flag is owned by the root user.
- But in this challenge, college_file's owner has been changed to the hacker user,so we must change ownership to retrieve the flag.
- hacker can do with it the same things that root had been able to do with it.
- Therefore we need to use the 'chown' command which helps us to change the ownership of files.
- After touching the 'college_file' file, we invoke 'chown hacker college_file' to change ownership where the /flag file is in order to get the flag.
- Flag: pwn.college{QFpJbIL1Jj7-epEIi9CwpYGlPNS.dFTM2QDL2ITO0czW}
# Groups and files
**Steps**
- In this challenge, the flag is readable by whatever group owns it, and this group is currently root.
- We must invoke 'chgrp' as the hacker user and change the group ownership of the flag file.
-  We find this out by using the 'ls -l /flag' command.
- Flag: pwn.college{c_WyFMsWT73hJdgq4dvBx549NE1.dFzNyUDL2ITO0czW}
# Fun with group names
**Steps**
- In this challenge, we will need to use the 'id' command to figure the name of the owner of flag, then chgrp to that owner.
- That is given by the 'gid'.
- Therefore in our case we invoke 'chgrp grp2517 /flag' and then read out the flag using 'cat /flag' command.
- This gives us the desired flag.
- Flag: pwn.college{UV4EV6GikUDi5Ch3Qhlu22VXOw0.dJzNyUDL2ITO0czW}
# Changing permissions
**Steps**
- Permissions for the owning user, 3 characters denoting the permissions for the owning group are user group and other.
- We can add or remove permissions for reading, writing or executing for user, group or other by invoking the command in this format 'chmod [OPTIONS] MODE FILE'.
- In this challenge, we must change the desired permissions of the /flag file to read it.
- Flag: pwn.college{A0BAeNzaa0qr58K12rEohiSfUUx.dNzNyUDL2ITO0czW}
# Executable files
**Steps**
- +/- x can be added as argument to u,g or o to execute or stop executing files.
- In this challenge, the /challenge/run program will give you the flag, but we must first make it executable by invoking +x argument to chgrp.
- Flag: pwn.college{UAVdmGVjohHsLEddZFd_KKIvJko.dJTM2QDL2ITO0czW}
# Permission Tweaking practice 
**Steps**
- In this challenge, we use the above knowledge to get through an 8 step long process of changing desired permissions to get the flag and read it.
- Flag: pwn.college{s0n8iVRo8Ns7h2lWsDr4Gh8qmCI.dBTM2QDL2ITO0czW}
# Permissions setting practice
**Steps**
- We can also set permissions to u, g or o by using the '=' sign by assigning the desired permissions instead of using +/- to make adding or removing permissions easier.
- Again, in this challenge, we go through an 8 step long process of assigning the desired permissions- r, w or x to finally read the flag and retrieve it.
- Flag: pwn.college{IBDSUvh4KHo5LvicWudxzTAcX9v.dNTM5QDL2ITO0czW}
# The SUID Bit
**Steps**
- The s part in place of the executable bit means that the program is executable with SUID. It means that, regardless of what user runs the program (as long as they have executable permissions), the program will execute as the owner user (in this case, the root user).
- As the owner of a file, you can set a file's SUID bit by using 'chmod: chmod u+s [program]'.
- In this challenge, '/challenge/getroot' is the file which we need to execute using the 'su' command.  
- Flag: pwn.college{0I0rSAR8oExCCQPOkvbXoxlz7vm.dNTM2QDL2ITO0czW}
