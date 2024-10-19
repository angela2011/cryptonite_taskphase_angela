# Becoming root with su
**Steps**
- In this challenge, we used the su (the switch user) command.
- The su command is SUID bit set, and hence su runs as root. Running as root, it can start a root shell.
-  In this challenge, it does have a root password. That password is 'hack-the-planet', and we must provide it to su to become root.
-  So after running the su command, it asks for the password which we input and finally gives us the flag.
- Flag: pwn.college{YBYPt1pmdCeaNWgclrz0jYceThU.dVTN0UDL2ITO0czW}
# Other users with su
**Steps**
- With no arguments, su will start a root shell. However, we can also give a username as an argument to switch to that user instead of root.
- In this challenge, we need to switch the username to zardus user instead of the root shell and then run /challenge/run. The zardus password is 'dont-hack-me' which we input once password is asked.
- After performing all these steps, we get the flag.
- Flag: pwn.college{U0yQ__PcnXVfNf54nO1IbEEVR58.dZTN0UDL2ITO0czW}
# Cracking passwords
**Steps**
- When we input a password into su, it one-way-encrypts (hashes) it and compares the result against the stored value. If the result matches, su grants us access to the user.
- But in this case, we use the 'john' command along with /challenge/shadow-leak as argument to get the password.
- This is done because if a hacker gets their hands on a leaked /etc/shadow, they can start cracking passwords and wreaking havoc. Here, John the Ripper cracked Zardus' leaked password hash to find the real value of password1337.
- After this, we run /challenge/run to get the flag.
- Flag: pwn.college{Au9L0XneMuy0tbp31u0SqoU1k2x.ddTN0UDL2ITO0czW}
# Using sudo
**Steps**
- Unlike su, rather than authenticating via password, sudo relies on policies that it checks to determine the user's authorization run things as root.
- In this challenge, we have sudo access, and we will use it to read the flag.
- Flag: pwn.college{88rYbz9GkGRTmBmrhfplJrhZaZh.dhTN0UDL2ITO0czW}
