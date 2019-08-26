# SHTACS Computer Science Setup
This readme will help you through the initial setup of your computer for the AP Computer Science A course.

# Part 1: (For Windows only) Windows Subsystem for Linux
In order to do some key things on the course, we need to install a program that gives us access to Linux. MacOS already has this build in. If you have OSX, please go to Part 2: Terminal.

First open the Windows Powershell in Administrator mode.

((Image of getting powershell))

Then copy the command:

```
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

and restart the computer when asked.

After the restart is complete, go into the Windows Store and search for 'Debian' and download it.

Once the download is complete, launch Debian and follow the instructions.

# Part 2: Terminal
The terminal is the most efficient way to navigate and use your computer.

For MacOS:
```
Control + Option + Shift + T
```

For Windows:

Open the Debian program.

# Part 3: Git
We use git and github for version control, projects and homework.

To install copy this command into the terminal:

Windows (WSL):
```
sudo apt install -y git
```

macOS:
```
xcode-select --install
```

Type to check it's good to go:
```
git --version
```

# Part 4: Github

Go to https://www.github.com and sign up for an account.

# Part 5: Add SSH key

Go to your terminal and paste in:
```
 ssh-keygen -t rsa -b 4096 -C "your_github_email@address.com"
```

Press enter three times until complete.

Once complete enter the following command:

macOS:
```
pbcopy < ~/.ssh/id_rsa.pub
```

WSL:
```
cat ~/.ssh/id_rsa.pub
```

For WSL, copy the output in the Terminal, in macOS it is already copied for you.

Now go to: https://help.github.com/en/articles/adding-a-new-ssh-key-to-your-github-account and follow the instructions.

To test input the following command in the Terminal:
```
ssh -T git@github.com
```
Once prompted, enter 'yes' and you should get a message saying "Hi username! You've successfully authenticated, but GitHub does not provide shell access".

# Part 6: IntelliJ

IntelliJ will be the IDE we will use for Java programming. Go to https://www.jetbrains.com/idea/download, download and install the 'Community Edition'.
