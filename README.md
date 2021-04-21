# IOChecker

The purpose of this tool is to help you to find out if your station is compromised or not by checking if the IOC’s you have previously found are exist on the station. This tool can check the following IOC’s types:
1.	Registry Keys – search by full key directory. 
2.	Scheduled Tasks – search by task name.
3.	Services – search by service name.
4.	Files – search by full file directory. 
5.	Processes – search by process name.

The tool is written in .Net and should run on any version of windows.

Use:

1.	Download both the .exe file(Download the file from **Release**) and config file.

Please pay attention: the exe and a config file have to be in the same directory for the tool to work.

2.	Open config file. it looks like that:<br/>
![Pic 1](https://github.com/genzsecurity/IOChecker/blob/17da785c5c070b0580f50a4927be9c512ff0c8a6/2.png)

3.	Just add your IOC’s to the correct value, like that:
![Pic 2](https://github.com/genzsecurity/IOChecker/blob/17da785c5c070b0580f50a4927be9c512ff0c8a6/3.png)

You can add several IOC’s that are the same type, just add another add key. The key should look exactly like the ones that already exist. Just edit the key name. Key name has to contain the type name(Registry/Task/Service/File/Process) and some other number.
While entering your IOC's to the config file, pay attention to the following:

* This tool is key sensitive. <br/>
* In case your IOC is a file directory, you need to add '\' in every place where it already exists, so it's going to become '\\.'<br/>
* In case your IOC is a process, write only the process name without any extensions(which means do not include file type, like exe, etc.).<br/>
* In case your IOC is registry key, change 'HKEY_CURRENT_USER' to 'HKCU' and change 'HKEY_LOCAL_MACHINE' to 'HKLM.'<br/>


4.	Now you can run the tool with administrator permissions. When it's done, you see the following window(may take several seconds after the console window disappears):
![Pic 3](https://github.com/genzsecurity/IOChecker/blob/17da785c5c070b0580f50a4927be9c512ff0c8a6/1.png)
