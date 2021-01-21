Experimental environment: win10 x64    
Software official website:https://sd.360.cn/   
Software version:5.0.0.5062    
Affected Component: 360rp.exe  C:\ProgramData\360SD\Quarant\360SD.Summary.union1    
  
Attackers can use symbolic links to write content to any file with system permissions (the content cannot be controlled) with sysytem permissions.    
If the target file is pci.sys, the computer will not start.     
If you write an antivirus protection program, the antivirus protection will be ignored.    

To exploit this vulnerability, you need to delete the Quarant directory, then create an object manager symbolic link to make \RPC Control\360SD.Summary.union1 point to the file name to be opened, and then create a directory link Quarant link to \RPC Control, and then start 360 Antivirus quick scan or full scan. You only need to wait a moment to write the target file.    

For example, the cmd command:    
CreateSymlink.exe "C:\ProgramData\360SD\Quarant\360SD.Summary.union1" "‪C:\Windows\System32\drivers\pci.sys"    
