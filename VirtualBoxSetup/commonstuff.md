# Enable OpenSSH Server on Windows

in admin powershell terminal: Get-WindowsCapability -Online | ? Name -like 'OpenSSH.Ser*'
in admin powershell terminal: Set-Service -Name sshd -StartupType 'Automatic' <--- automatically starts sshd at StartupType

# Mount windows folder to VirtualBox running linux

## VirtualBox Settings

1. Right click machine
2. Click shared folders
3. Transient = just for session, machine = forever
4. add folder <vboxfoldername>

## Guest Linux OS

Next on the the guset OS make a directory to use for your mount preferably in your home directory.
1. mkdir {sharedfoldername}
2. in linux VM: sudo mount -t vboxsf {vboxfoldername} {sharedfoldername}
