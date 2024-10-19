# The PATH Variable
**Steps**
- In this level, you will disrupt the operation of the /challenge/run program. This program will DELETE the flag file using the rm command.
- We need to make it such that make it so that /challenge/run also can't find the rm command.
- To do this callenge, we must blank out PATH like PATH=" " so that when running /challenge/run, bash cannot find the rm command's program.
- Flag: pwn.college{45f920EyyP_NzS96UCSBRxKPUm5.dZzNwUDL2ITO0czW}
-
-


# Setting path
**Steps** 
- if we want to run programs, we could just add their directories to the PATH variable.
this allows us to run them without using their entire path and instead by using only their name.
- to run win, I had to overwrite the current PATH to include the directory that the win command resides in.

- Flag: pwn.college{8Za_L2h92IcDSpOvkFBrB8hcYyl.dVzNyUDLwIzN0czW}
# Adding commands
**Steps** 
- We need to find location of cat for which I learnt about the which command.
- Then make win script such that it cats the flag using location of cat.
- After that we add the win script to PATH without overwriting PATH. for this we need to append :$PATH adds the directory to PATH without removing its previous directories. Then I simply run the /challenge/run file.
- Flag: pwn.college{kRwvgJclsVWiQRvn3Ps8s3vwM7K.dZzNyUDLwIzN0czW}
# Hijacking commands
**Steps** 
- For this task we have to make my own rm command so that when the PATH variable is searched, it uses the directory in which my command lies, instead of the original one.
- Flag: pwn.college{4G6IQstrwRsR7OkAZzEbldnfKH7.ddzNyUDLwIzN0czW}

