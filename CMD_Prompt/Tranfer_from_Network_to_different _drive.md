#Transfer Files from a Network drive to a local drive


##Windows 7
In order to prevent from having to run a copy paste through windows explorer and sit through the pre copy step of "Processing files", You can use robocopy.

[Microsoft docs here](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/robocopy)

I ran into a problem on the command line with robocopy that prevented me from being able to go directly to the Network drive.

I was able to map the drive locally.

1. Open Computer by clicking the Start button and then clicking Computer.
2. Click Map Network Drive.
3. In the Drive list, click any available drive letter.
4. In the Folder box, type the path of the folder or computer, or click Browse to find the folder or computer. To connect every time you log on to your computer, select the Reconnect at logon check box.
5. Click Finish.

[Mapping info here](https://support.microsoft.com/en-us/help/4026635/windows-map-a-network-drive)