---
title: "Python venv"
excerpt: Using virtual environments in Python.
published: true
---

!["Python Virtual Environments (venv)"](/images/python-logo-for-blog.png)

Python employs Virtual Environments (venv) to isolate environments and the components that are contained within those environments. This allows developers to run their code under multiple sets of conditions - for example, one environment might have a specific module installed, like beautifulsoup4, whereas another might have beautifulsoup3. By running the code in both of these isolated environments, the developer can identify and mitigate failure points in the code; making their code more robust in the process. 

The official Python documentation on the topic can be found at [https://docs.python.org/3/library/venv.html](https://docs.python.org/3/library/venv.html).

Here are the high-level steps for setting up venv: 







| Platform | Shell  | Command |
|----------|--------|---------|
|Posix	   |bash/zsh|$ source <venv>/bin/activate|
|          |fish	  |$ . <venv>/bin/activate.fish|
| 	       |csh/tcsh|$ source <venv>/bin/activate.csh|
|Windows	 |cmd.exe	|C:\> <venv>\Scripts\activate.bat|
| 	       |PowerShell|PS C:\> <venv>\Scripts\Activate.ps1|
