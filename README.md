Experimental environment: win10 x64   
Software official website:https://sd.360.cn/
Software version：5.0.0.5062  
Affected Component: 360rp.exe  C:\ProgramData\360SD\Quarant\360SD.Summary.union1   
  
Attackers can use symbolic links to write content to any file with system permissions (the content cannot be controlled) with sysytem permissions.   
If the target file is pci.sys, the computer will not start.   
If you write an antivirus protection program, the antivirus protection will be ignored. 

To exploit this vulnerability, you need to delete the Quarant directory, then create a symbolic link to the file name to be written, and then start the 360 antivirus quick scan, you only need to wait a moment, the target file will be written   
