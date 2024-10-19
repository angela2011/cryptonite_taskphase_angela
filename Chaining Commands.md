# Chaining commands
**Steps** The easiest way to chain commands is ;. In most contexts, ; separates commands in a similar way to how Enter separates lines.
- In this case I had to run /challenge/pwn and then /challenge/college seperated by a ';'.
- This got me the flag.
- Flag: pwn.college{IonoLyRJy6BuNnWZXBHxc_A9lKD.dVTN4QDL2ITO0czW}
# Your first shell script
**Steps**
- If we want to run many commands in a consecutive manner, we can store them in a file called shell script.
- The shell scripts have suffix .sh and to invoke the script, we use bash as command.
- In this challenge, (I referred to https://www.geeksforgeeks.org/how-to-create-a-shell-script-in-linux/ as I didnt know how to create the shell script and is not mentioned in pwn collegte.)
from this site I learnt that I needed to:
  -create the script using touch command
  -make it executable by changing mode using chmod command
  -use a text editor (I used nano) to type the commands in the script
- After that, one must use the 'bash x.sh' command in the terminal to get the flag.
- Flag: (Flag could not be obtained due to an issue in the next 3 problems. Steps are written according to the website I referred to)
# Redirecting Script Output
**Steps**
- If we want to redirect multiple outputs to one command's input, we could store them in a script and then pipe the same shell script to the command's input.
- Since we had already created the script containing the commands required for this challenge, all we have to do is pipe it into the input of /challenge/solve to obtain the flag.
- Flag:
# Executable shell scripts
**Steps** 
- When we use the bash command we're basically telling the shell to read the commands from the argument script.
- Here the file is already executable then we can just run it without "bash" ie we just use it's absolute/relative path.
- In this challenge,  we need to create a script of our choice where we will store the program /challenge/solve. Then we can use the 'chmod' command to make it executable and then we will be able to run it using its relative path.
-  Flag:
