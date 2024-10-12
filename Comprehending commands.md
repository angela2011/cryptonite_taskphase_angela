# Cat not the pet, but the command
**Steps:** The cat command is used for reading out files.
So in this case the flag is read using the cat command which was stored in the flag file.
Flag: pwn.college{gorDt9kbTIJlmSzT_v4gOGmV8he.dFzN1QDL2ITO0czW}
# catting absolute paths
**Steps:** Same steps as previous one except that the absolute path of flag was used.
Flag: pwn.college{cTKP4-NQMyB-VDTUM10zxmvZtHa.dlTM5QDL2ITO0czW}
# More catting practice
**Steps:** As cd directory cannot be used, absolute path of the file is used (in this case it is: /usr/share/cargo/flag ).
-Therefore 'cat /(file name )' is invoked.
Flag: pwn.college{wVtgCREta0JysGzQW_O1thKGql9.dBjM5QDL2ITO0czW}
# grepping for a needle in haystack
**Steps:** The grep command is used to search for the contents we need. In this case we need to search for the flag.
-As we know by now, the flag always starts with pwn.college, we grep for the same.
flag: pwn.college{gS1LbI5IC0UxCKn0SQY8yBDp6SO.ddTM4QDL2ITO0czW}
# Listing files
**Steps:**  To list the contents of a particular file, the ls command is used.
-In this case, we need to look for the /challenge/run file by listing the files in /challenge and then finding it.
Flag: pwn.college{wtAruHpJEeIlV4FW58plAc3UCNl.dhjM4QDL2ITO0czW}
# Touching files
**Steps:** We can create a new, blank file by touching it using the touch command. 
-In this challenge, two files /tmp/pwn and /tmp/college are created by using the touch command and /challenge/run is run to get the flag.
Flag: pwn.college{wss1GOUQ5hcFelbPKpLkyxUOZSG.dBzM4QDL2ITO0czW}
# Removing files
**Steps:** The rm command is used to remove files.
-In this challenge, delete_me file in the home directory had to be removed using the rm command and then /challenge/run is run in order to get the flag.
Flag: pwn.college{AkKoFhjVBpU7a2IXfSJjI23YlN6.dZTOwUDL2ITO0czW}
# Hidden files
**Steps:** ls doesn't list all the files by default so ls -a is used to show the hidden files.
Flag: pwn.college{Y-urAJk35MY1XGTbuztnuPia6-z.dBTN4QDL2ITO0czW}
# An epic filesystem quest 
**Steps:** By using cd, ls, and cat to solve a repetetive list of challenges.
-For the last two challenges we must be careful about not changing into the directory.
# Making directories
**Steps:** We can make directories using the mkdir command. By creating /tmp/pwn directory the flag was obtained in this challenge.
Flag: pwn.college{owOhgbo6UwkmtSo76vHBIAw1-VU.dFzM4QDL2ITO0czW}
# Finding files 
**Steps:** For every file whose permission is not denied, we need to search for the flag using the find command. The process is continued until we find the flag.
Flag: pwn.college{k4jcpmeiREMkecv77p9c7X-U6gz.dJzM4QDL2ITO0czW}

**Steps:*
Flag: pwn.college{At_d_wKYffINAEkxQeTgNIyDex3.dljM4QDL2ITO0czW}



