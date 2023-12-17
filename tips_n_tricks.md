# My personal repo containing tips, tricks, and handy snippets of information


## Some random stuff
Edmonton Lunch List Restaurants
http://in/edm_restaurants


To check the size of all the directories, recursively:
```
du -hs *
du -hs * | grep "G\t"
```

To search for a file by name, recursively:
```
find . -name "foo*"
```

To deal with mobile backups (so that Insync doesn't back them up):
```
Move files:
mv ~/Library/Application\ Support/MobileSync/Backup/* ~/dev/personal/Archive/mobile/
Move them back:
mv ~/dev/personal/Archive/mobile/* ~/Library/Application\ Support/MobileSync/Backup/

Symbolic link: 
  -- first delete the ~/Library/Application\ Support/MobileSync/Backup directory, and its contents
ln -s ~/dev/personal/mobile/Backup/ ~/Library/Application\ Support/MobileSync/
```

To verify a GPG signature:
```
1. Download the <file> and its signature <file>.asc.txt
2. Download the public <key>.asc.txt
2. gpg --import <key>.asc.txt
3. gpg --fingerprint    # Verify this against an independent source
4. gpg --verify <file>.asc.txt <file>
5. gpg --list-keys
6. gpg --delete-key <fingerprint without spaces>
7. rm <file>.asc.txt
8. rm <key>.asc.txt
```

Running VMWare on Big Sur. Having trouble with internet access?
```
Open Control Panel from VM
Click Network & Sharing Center
Click Ethernet Adapter
Click Properties
Click TCP/IPV4 Properties
Set Preferred DNS Server to 172.22.67.241 then click OK
Click OK again
```
