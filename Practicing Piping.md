# Redirecting output
**Steps:** In this challenge, we must use the '>' input redirection to write the word PWN to the filename COLLEGE.
- Hence 'echo PWN > COLLEGE' needs to be invoked.
- Flag: pwn.college{Yq9AjFDTNCkDjrju7MhF-f-y5Lf.dRjN1QDL2ITO0czW}
# Redirecting more output
**Steps:** In this challenge the flag is recieved only when the output of /challenge/run is redirected to myflag.
- Hence the same logic is used as that of the previous question, to get the flag.
- Flag: pwn.college{Up2laSyIxm9zmXAF8mjcOOr5hDN.dVjN1QDL2ITO0czW}
# Appending output
**Steps:** We can now redirect input in append mode using >> instead of > (truncated mode).
- This is done so that when more than one file needs to be redirected, it does not get re written by the other file.
- In this challenge, challenge/run needs to be run with an append-mode to redirect it's output to the file /home/hacker/the-flag to get the flag.
- Flag: pwn.college{EXQHzb_0Z5JGva8fT0K3ehYEErQ.ddDM5QDL2ITO0czW}
# Redirecting errors 
**Steps:** '/challenge/run 2> instructions' needs to be invoked. This will redirect standard error (FD 2) to the instructions file.
- Finally, the output needs to be redirected to myflag where it will store the flag and display it.
- Flag:  pwn.college{sLcbu2jEnp0f-LLsXJebBbsUvWo.ddjN1QDL2ITO0czW}
# Redirecting input
**Steps:** The exact opposite sign '>' as that used to redirect output is used to redirect input.
- In this challenge, we need to redirect the PWN file to /challenge/run and have the PWN file contain the value COLLEGE.
- Flag: pwn.college{0G2HLtpNX8GsT0qpwGzMoGad572.dBzN1QDL2ITO0czW}
# Grepping stored results
**Steps:** We have already learnt that grep can be used to search for a particular word.
- The only difference is that we are now using this command in a redirected path to search for the flag.
- Flag: pwn.college{k2oehOjHoWgAqi4D1yyRGoRQgWG.dhTM4QDL2ITO0czW}
# Grepping live output
**Steps:** In this challenge, we are using the '|' (pipe) operator to grep for the flag.
- For instance 'echo /challenge/run | grep pwn.college' will highlight the flag among the thousand lines in /challenge/run.
- Flag: pwn.college{gAtUzE73R-CZwiOfgRkUuHE7TJR.dlTM4QDL2ITO0czW}
# Grepping errors
**Steps:** In this challenge, we redirect standard error to standard output (2>& 1) and then pipe the now-combined stderr and stdout using '|'.
- This challenge is a combination of previous 2 challenges.
- Flag: pwn.college{ogpNnBy5A5tkM1Sq_aJpQp0Qjm1.dVDM5QDL2ITO0czW}
# Duplicating piped data with tee
**Steps:** The tee command, named after a "T-splitter" from plumbing pipes, duplicates data flowing through your pipes to any number of files provided on the command line.
- In this challenge, using the tee command, /challenge/pwn must be piped into /challenge/college.
- Catting the output of the /challenge/pwn file, we learn that --secret argument must be used to get the flag.
- Flag: pwn.college{IavCZiIlmxnaFHO2CadD7CIt9i5.dFjM5QDL2ITO0czW}
# Writing to multiple programs
**Steps:**
- Process substitution is a method used to transfer the output of one command to the input of multiple other commands.
- It basically treats the output of any command as a file, which is given a file name aka a named pipe.
the >() operator signified proces substitution ie anything inside it is treated like a file.
- With the tee command, we need to use the >(/challenge/the) to take the output of the initial program and use it as the stdin here.
- 
