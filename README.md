## [I'm here by mistake! Take me to the profile page.](https://github.com/tzucker02)

# Create a virtual environment for each Python Project

Virtual environments in Python create isolated spaces for your projects, preventing package conflicts and keeping your system Python clean. They're essential for managing dependencies reliably across different tasks.

I am compiling some pros and cons to having a virtual environment for each Python project you start. So far here is what I have:
<p><i>(NOTE: This written for users of Windows OS boxes. I will be writing more for MAC users)</i></p>

## Pros
There a several reasons you should absolutely use virtual environments. 

- <b>Dependency Isolation</b>: Different projects can use specific package versions (e.g., one needs requests 2.25, another 2.31) without clashes.
- <b>System Protection</b>: Avoids polluting the global Python installation, which could break OS tools or get overwritten during updates.
- <b>Reproducibility</b>: Pin exact dependencies via requirements.txt, making it easy to replicate setups for teams or deployment.

Global installs lead to version mismatches, privilege issues (needing sudo), and hard-to-debug errors. Virtual environments sidestep these by containing everything per project.

## Cons
- <b>Extra Complexity</b>: Beginners face a learning curve for setup, activation, and management, adding steps to daily workflows.
- <b>Disk Space</b>: Each environment duplicates Python and packages, consuming storage—especially with large libraries like TensorFlow.
- <b>Activation Hassle</b>: Forgetting to activate leads to errors; must repeat per session or project switch.

## How to create a virtual Environment
There are several fairly simple steps in making a virtual environment. So if you have decided that this is the best course for you, they are as follows:
### 1. Start a command prompt
 - This is the first step, and not very difficult. If you are used to using a Windows machine, then you have probably done this more than once. 
 - Start by clicking on the windows icon (usually located on the far left of the toolbar). 
 - Type the command ```cmd.exe``` and press ```enter```
 - You have successfully started the command program when the black screen pops up on your screen. Note that this will often default to the working directory of the logged in user (c:\users\<logged-in-user-name> followed by a greater than sign, e.g. c:\users\owner>)
### 2. Navigate to the directory where you wish to create the virtual environment
 - If you want to create your virtual environment in the current directory, you need to do nothing at all.
 - If you want to create your virtual environment in another directory, you need to use the CD command to navigate to that directory before going forward. For instance, if you want to create the virtual directory in c:\users\owner\documents, use the command ```cd Documents```, or ```cd c:\users\owner\documents```.
### 3. Use the command: 
```python -m venv <name of venv>``` at the command prompt
 - You are still in the ```cmd.exe``` command processor. 
 - You should see a screen something akin to the screenshot below:
<img width="289" height="160" alt="image" src="https://github.com/user-attachments/assets/2ae627b0-d1c4-4034-b480-af661753059a" align="center"/>

 - Type in the command as it appears above,  substituting the name of the virtual environment you wish to create.
### 4. Activate the virtual environment using the command 
```./<virtual-environment-name>/Scripts/activate``` </b>
(e.g. ./tz_medium/Scripts/activate or just tz_medium /Scripts/activate)</b>
On a MAC issue the command</b> ```source myenv/bin/activate```
### 5. Use the [requirements.txt](https://github.com/tzucker02/Virtual_environment/blob/main/requirements.txt) file to duplicate my current environment in your new virtual environment.
 - After the step above, activating your virtual environment, go to the next step.
 - Use the command
```pip install -r requirements.txt```

You have now created a new virtual environment, activated it and installed the requirements for the projects noted here. To get out of the virtual environment, and restore your usual prompt, simply give the command ```deactivate``` and press ```enter```.
