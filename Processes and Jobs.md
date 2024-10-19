# Processes and jobs
**Steps** 
- These two methods, ps -ef and ps aux list down different processes running in our terminal.
- But ps -ef and ps aux result in slightly different, but cross-recognizable output.
- These commands are a result of the following individual commands-
- e to list "every" process and -f for a "full format".
- a to list processes for all users, x to list processes that aren't running in a terminal, and u for a "user-readable" output.
- /challenge/run is changed to a random filename, and this time it is made such that we cannot ls the /challenge directory.
- After using ps aux we can retrieve the flag.
- Flag: pwn.college{0L9Ww6oqR6Cd6k5GUbKQlJcM_DV.dhzM4QDL2ITO0czW}
# Killing processes
**Steps** 
- We use the 'kill' command to terminate it by passing the process identifier (the PID from ps) as an argument.
- In this challenge we find the 'dont_run' process from /challenge/pwn.college and terminate it using the kill command.
- After that we will run the /challenge/run command to obtain the flag.
- Flag: pwn.college{oe0GQzJ266-b7q80fqlDSoNUxCO.dJDN4QDL2ITO0czW}
# Interrupting processes
**Steps** 
- The Ctrl-C key (e.g., holding down the Ctrl key and pressing C) sends an "interrupt" to whatever application is waiting on input from the terminal and, typically, this causes the application to cleanly exit.
- In this challenge, we will interrupt /challenge/run to get the flag.
- Flag: pwn.college{wNiAvDO1lenQb2rVjqVDLuQKog3.dNDN4QDL2ITO0czW}
# Suspending processes
**Steps** 
- We can suspend processes to the background with Ctrl-Z key.
- In this challenge, run wants to see another copy of itself running and using the same terminal. We need to use the terminal to launch it, then suspend it, then launch another copy while the first is suspended.
- After performing the processes in the correct sequential order, we retrieve the flag.
- Flag: pwn.college{ckXIpWEduuTXQd34Tuc1z13L_19.dVDN4QDL2ITO0czW}
# Resuming processes
**Steps** 
- To resume processes, your shell provides the fg command, a builtin that takes the suspended process, resumes it, and puts it back in the foreground of your terminal.
- We need to invoke 'fg' and the read the flag.
- Flag: pwn.college{gEPaNt1AD4La0UR4AdcRjSrRZoF.dZDN4QDL2ITO0czW}
# Background processes
**Steps** 
- We can also resume processes in the background with the bg command. This will allow the process to keep running, while giving us our shell back to invoke more commands in the meantime.
- So in this challenge, we will pwrform the same steps from our previous knowledge but instesd of passing the fg command, we will pass the bg command and get the flag.
- Flag: pwn.college{4_BeE6rCs5cn-6qu5Jo0a2iCgxT.ddDN4QDL2ITO0czW}
# Foreground processes
**Steps** 
- We will foreground a backgrounded process with fg just like we foreground a suspended process.
- The steps are the same and we obtain the flag.
- Flag: pwn.college{0r7FAmGMXfnZXc0xxGGaT9SoPmo.dhDN4QDL2ITO0czW}
# Starting background processes
**Steps** 
- To start a background proces, all you have to do is append a & to the command, to the file '/challenge/run' backgrounded for the flag in the given format-
- /challenge/run [PID] &
- Flag: pwn.college{MGfgo4nK_SQ2MAQ7XE2ZdiDK73N.dlDN4QDL2ITO0czW}
# Process exit codes
**Steps** 
- We can access the exit code of the most recently-terminated command using the special '?' variable like so: 'hacker@dojo:~$ echo $?' on the terminal.
- Commands that succeed typically return 0 and commands that fail typically return a non-zero value, most commonly 1.
- In this challenge, we use the number that is returned as an argument with /challenge/submit-code. In my case the number returned was 27.
- Flag: pwn.college{QmCKQOwvYwSK06UYypWWFZR4uu0.dljN4UDL2ITO0czW}
