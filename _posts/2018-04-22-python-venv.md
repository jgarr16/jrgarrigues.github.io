---
title: "Python venv"
excerpt: Using virtual environments in Python.
published: true
---

!["Python Virtual Environments (venv)"](/images/python-logo-for-blog.png)

Python employs Virtual Environments (venv) to isolate environments and the components that are contained within those environments. This allows developers to run their code under multiple sets of conditions - for example, one environment might have a specific module installed, like beautifulsoup4, whereas another might have beautifulsoup3. By running the code in both of these isolated environments, the developer can identify and mitigate failure points in the code; making their code more robust in the process. 

The official Python documentation on the topic can be found at [https://docs.python.org/3/library/venv.html](https://docs.python.org/3/library/venv.html).

What follows is the high-level steps for setting up venv in a Python 3 environment: 

1. Enable the venv:
   
   (*note: venv does not need to be installed as it is a standard component in Python 3*)

   ```blunderboy:~ python3 -m venv <name_of_vir_env>```

2. Activate the venv - *note the addition of the venv name after activation*:

   ```blunderboy:~ source <name_of_vir_env>/bin/activate
   (<name_of_vir_env>) blunderboy:~ ```
   
   (*other operating systems will need to use commands for their particular OS*)


   | Platform | Shell  | Command |
   |----------|--------|---------|
   |Posix	   |bash/zsh|$ source <venv>/bin/activate|
   |          |fish	  |$ . <venv>/bin/activate.fish|
   | 	       |csh/tcsh|$ source <venv>/bin/activate.csh|
   |Windows	 |cmd.exe	|C:\> <venv>\Scripts\activate.bat|
   | 	       |PowerShell|PS C:\> <venv>\Scripts\Activate.ps1|
   
3. 
