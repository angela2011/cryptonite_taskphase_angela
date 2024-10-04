# **The Root**
**Steps:** 
The path that starts with the root directory(in this case:/pwn) is the absolute path. Hence /pwn is invoked.
     Flag: pwn.college{UMgcz8RFgj-oePZ4CHWD0FKElzh.dhzN5QDL2ITO0czW}
# **Program and absolute paths**
**Steps:** 
This challenge needs to be executed by invoking its absolute path.
So we have to execute the run file that is in the challenge directory that is, in turn, in the / directory.
hence /challenge/run is invoked
     Flag: pwn.college{oddb4xAP0jAiAO3DNLSUL___4eU.dVDN1QDL2ITO0czW}
# **Position thy shelf**
**Steps:** 
Ater executing the /challenge/run program, the terminal mentions a specefic directory to which it has to be changed. Hence "cd (file name)" is invoked.
     Flag: pwn.college{c8HeV3NwXAdTFW01KRWDNdBCm1m.dZDN1QDL2ITO0czW}
# **Position elsewhere**
**Steps:** 
same as previous
     Flag: pwn.college{Y6-3SW7eBuKKIVe08kzZpFHG7eN.ddDN1QDL2ITO0czW}
# **Position yet elsewhere**
**Steps:** 
same as previous
     Flag: pwn.college{Eh1o3H7bbGK2-jeoUONvcNPyx3l.dhDN1QDL2ITO0czW}
# **implicit relative paths, from /**
**Steps:**  
After learning the concept of relative path and relation with parent path,
To run /challenge/run using a relative path while having a current working directory of /
relative path starts with the letter c
Hence cd /, challenge/run needs to be invoked as relative path starts with c.
     Flag: pwn.college{Qr7V6TisIXLQiuLhZ-N3ZlMKmUX.dlDN1QDL2ITO0czW}
# **Explicit relative paths, from /**
**Steps:** 
As '.' refers right to the same directory,
'./' also refers to the same directory, and so on
./challenge/run needs to be invoked
     Flag: pwn.college{giBFPKkG4Shc8mvg8D9XpiXYQdU.dBTN1QDL2ITO0czW}
# **Implicit relative paths**
**Steps:**  
One could accidentally execute programs in the current directory that happened to have the same names as core system utilities and that's why in this case run is expressed as a relative path
By using implicit relative path a './' can be used before run
Therefore after cd, ./run is invoked.
     Flag: pwn.college{oqV2wbV448RK6FxeaDsjI_Hfr9_.dFTN1QDL2ITO0czW}
# **Home sweet home**
**Steps:** 
'/challenge/run ~' is invoked to make an absolute argument
cd is invoke as it changes directory to /home/hacker by default
as total characters need to be less than 3, ~/~ is used as absolute argument in the home directory to finally find the flag
     Flag: pwn.college{09y6geD9YesUi3yWWuATTuQzzvT.dNzM4QDL2ITO0czW}
