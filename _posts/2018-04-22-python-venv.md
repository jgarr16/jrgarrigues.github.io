---
title: "Python Virtual Environments (venv)"
excerpt: Using virtual environments in Python.
categories: tech
thumbnail: wrench
published: true
---

!["Python Virtual Environments (venv)"](/images/python-logo-for-blog.png)

Python employs Virtual Environments (venv) to isolate environments and the components that are contained within them. This allows developers to run their code under multiple sets of conditions - for example, one environment might have a specific module installed, like beautifulsoup4, whereas another might have beautifulsoup3. By running the code in both of these isolated environments, the developer can identify and mitigate failure points in the code; making their code more robust in the process. 

The official Python documentation on the topic can be found at [https://docs.python.org/3/library/venv.html](https://docs.python.org/3/library/venv.html).

What follows is the high-level steps for setting up venv in a Python 3 environment: 

1. Enable the venv:
   
   (*note: venv does not need to be installed as it is a standard component in Python 3*)

   ```blunderboy:~ python3 -m venv <name_of_vir_env>```

2. Activate the venv - *note the addition of the venv name after activation*:

   ```blunderboy:~ source <name_of_vir_env>/bin/activate```

   ```(<name_of_vir_env>) blunderboy:~ ```
   
   (*this guide is for MacOS, other platforms will need to use commands for their particular OS*)


   | Platform | Shell  | Command |
   |----------|--------|---------|
   |Posix|bash/zsh|$ source <venv>/bin/activate|
   | |fish|$ . <venv>/bin/activate.fish|
   | |csh/tcsh|$ source <venv>/bin/activate.csh|
   |Windows|cmd.exe|C:\> <venv>\Scripts\activate.bat|
   | |PowerShell|PS C:\> <venv>\Scripts\Activate.ps1|


3. For good measure, update PIP:

   ```(<name_of_vir_env>) blunderboy:~ pip install --upgrade pip```
   
4. Run *pip list* to see what modules are installed in the venv:

   ```(<name_of_vir_env>) blunderboy:~ pip list```
   
5. Install the packages that you need for the environment:

   ```(<name_of_vir_env>) blunderboy:~ pip install beautifulsoup4```
   
6. To quit the virtual environment, you can deactivate it: 

   ```(<name_of_vir_env>) blunderboy:~ deactivate```
   
   or, you can activate another venv (if it is already established):
   
   ```(<name_of_vir_env>) blunderboy:~ source <name_of_next_vir_env>/bin/activate```
      
   ```(<name_of_next_vir_env>) blunderboy:~ ```
   
7. Finally, if you want to delete the virtual environment, deactivate any venv that you are in, and list the files in the directory. You will see all named venvs. To delete, simply run a recursive remove *rm -r <venv>*:
   
   ```(<name_of_next_vir_env>) blunderboy:~ deactivate```
   
   ```blunderboy:~ ls -al```
   
   ```blunderboy:~ rm -r <name_of_next_vir_env>```
   
If all goes well, you should be looking at something like this: 

!["Python venv sample"](/images/venv_show.png)
    
