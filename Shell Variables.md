# Printing variables
**Steps:** To access variables, '$' is used and henceprepending '$' infront of any variable gives us the value of that particular variable.
- In this challenge, we need to know the value of the variable FLAG. Hence, 'echo $FLAG' is invoked.
- Flag: pwn.college{Qmr4yNv4LXEHSPx-bDRI7FJ4Tau.ddTN1QDL2ITO0czW}
# Setting variables
**Steps:** In order to set the value of a variable we use the '=' operator.
- In this case PWN needs to have a value of COLLEGE.
- Hence 'PWN=COLLEGE' is invoked.
- Flag: pwn.college{oqZD30mQVpPS3URBqyVj5H45BKH.dlTN1QDL2ITO0czW}
# Multi word variables
**Steps:** To set more than one value (word) to a variable, quotes need to be used("").
- In this case, PWN is set to COLLEGE YEAH by assigning like this:PWN="COLLEGE YEAH" and the flag is obtained. 
- Flag: pwn.college{8gWyw-yPX6pu944h3_kW8suPOv3.dBjN1QDL2ITO0czW}
# Exporting variables
**Steps:** PWN needs to be set to the value COLLEGE and must be exported.
- COLLEGE needs to be set to the value PWN but should not be exported.
- After this we run /challenge/run and the flag is obtained.
- Flag: pwn.college{oveIWt_CMdTZBDVKqkqy_RHbENo.dJjN1QDL2ITO0czW}
# Printing exported variables
**Steps:** env command is used to print all exported variables.
- By going through the output, we find the value of flag.
- Flag: pwn.college{8A_1lMGPJZpiVJJ24Y2HsOKEYp_.dhTN1QDL2ITO0czW}
# Storing command output
**Steps:** 
- Flag:
# Reading input
**Steps:** 
- Flag: pwn.college{kugAyo6wjXtEsL7R5xfB2V03lyu.dhzN1QDL2ITO0czW}
# Reading files
**Steps:** 
- Flag: pwn.college{cGYJrYcWW5e0iTBHImj7rBzV_1-.dBjM4QDL2ITO0czW} 
