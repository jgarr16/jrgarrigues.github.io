---
title: "Managing Python Packages"
excerpt: A method for identifying packages installed in your Python environment.
categories: tech
thumbnail: wrench
published: true
---



`>>> import pkg_resources`
`>>> installed_packages = [(d.project_name, d.version) for d in pkg_resources.working_set]`
`>>> print(installed_packages)`
`[('XlsxWriter', '1.0.2'), ('wxPython', '4.0.1'), ('wheel', '0.30.0'), ('wcwidth', '0.1.7'),` 
`('urllib3', '1.22'), ('six', '1.11.0'), ('setuptools', '39.0.1'), ('requests', '2.18.4'), `
`('python-dateutil', '2.7.0'), ('pyperclip', '1.6.0'), ('pyflakes', '1.6.0'), ('pycryptodome',`
`'3.5.1'), ('pycodestyle', '2.3.1'), ('pip', '10.0.1'), ('mccabe', '0.6.1'), ('idna', '2.6'), `
`('ftfy', '5.3.0'), ('flake8', '3.5.0'), ('chardet', '3.0.4'), ('certifi', '2018.4.16'), `
`('bs4', '0.0.1'), ('beautifulsoup4', '4.6.0')]`
