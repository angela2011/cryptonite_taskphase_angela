# Matching with *
**Steps** When it encounters a * character in any argument, it will replace that argument with any files that match the pattern.
-For instance, file_ab can be replaced with file_*
Flag: pwn.college{QN4-7-1QxS-asAIYys3JhXFuj00.dFjM4QDL2ITO0czW}
# Matching with ?
**Steps** Has the same working algorithm as that of * except that ? can replace only one letterat a time. 
-For example, file_a can be replaced with file_? but file_ab cannot.
Flag: pwn.college{QirCAFpeQY0YSHJOpJT7snAOfpt.dJjM4QDL2ITO0czW}
# Matching with []
**Steps** Subset of potential characters, are specified within the brackets.
-For example, [abc] will match the character a, b, or c.
-In this case, file_b, file_a, file_s, and file_h can be represented as file_[bash].
Flag: pwn.college{Mh0XBi8x7iDRMeMcQ_KHdV7NexZ.dNjM4QDL2ITO0czW}
# Matching paths with []
**Steps** In this challenge, we need to run /challenge/run with a single argument that bracket-globs into the absolute paths to the file_b, file_a, file_s, and file_h files.
- The algorithm is same as that in the previous case and file[bash] is invoked as an argument after /challenge/run command.
# Mixing globs
**Steps** By using the globbing we've learned that is '*', '?', '[]' an argument needs to be globbed that will match the files "challenging", "educational", and "pwning"!
Flag:
# Exclusionary globbing
**Steps** In this challenge, /challenge/run needs to be run with all files that don't start with p, w, or n. This can be done by invoking a ! before naming the files inside [].
Hence [!pwn] needs to be invoed.
Flag:
