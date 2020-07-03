





what ports are listening on mac:
* $ lsof -i -P | grep -i "listen"

If you want to see it for all users, you’ll have to use sudo.
* $ sudo lsof -i -P | grep -i "listen"


Basic stuff for newbies:

view contents of any file:
$   cat <path to file>
 
change folders:
$  cd <folder path> 

list folder contents:  
$  ls

list folder contents in list format:  
$  ls -l

list folder contents, including hidden onest:  
$  ls -a

list folder contents in list format including hidden files:  
$  ls -l -a
you can simply combine them as follows, fyi:   
$  ls -la 

Run the same command again:
$  !! 
if needing to use sudo, then $  sudo !!  



Other stuff:

Start a simple Web Server in any folder:
$  python -m SimpleHTTPServer 8000
then you can navigate in your browser to the page you wish.  
E.G:  http://localhost:8000/test.html  
( to cancel just do Ctrl+C - may need to do it 2x)


Shutdown your Mac, with or without a delay:  
$  sudo shutdown -h now  

Restart your Mac immediately: 
$  sudo shutdown -r now  
 
Restart your Mac with time delay: 
$  sudo shutdown -r +60   

Create a file of any size:  
$  mkfile 1g test.docx
(makes a file of 1gig size - good for testing)
(b=bytes, k=kilobytes, m=megabytes, g=gigabytes)

Continually monitor the output of a file:
$  tail -f <path to file>
( Cancel this by doing Ctrl+C ) 

Get your network IP Address:  
$  ipconfig getifaddr en0

Show file contents:
$  cat <filename> 

copy folder contents from one location to another:
$  ditto -V ~/original/folder/ ~/new/folder/

download files outside of your browser:  
cd ~/Downloads/
curl -O http://www.thefilename.com/thefile/url.mp3

Create a custom login message:
$  sudo defaults write /Library/Preferences/com.apple.loginwindow LoginwindowText "In case of loss, call 555-555-5555."

How long has my Mac been running?
$  uptime 

Keep your Mac awake
$  caffeinate
End it by entering Ctrl+C.

You can create a set number of seconds before your Mac sleeps too: 
$  caffeinate -u -t 5400

Make your Mac automatically restart after a crash:  
$  sudo systemsetup -setrestartfreeze on

Add spacers to your Dock:
$  defaults write com.apple.dock persistent-apps -array-add '{"tile-type"="spacer-tile";}'
$  killall Dock
Repeat this command for each spacer you'd like for your Dock. To remove a spacer, you can drag it out to the right until you see the poof icon.


Dull Hidden apps on your Dock:
$  defaults write com.apple.Dock showhidden -bool TRUE
$  killall Dock
For apps that are hidden on your desktop, this will dull the icons for them on the Dock.  Useful to see apps you have not used in a while.  

Hide non-active apps on your Dock:
$  defaults write com.apple.dock static-only -bool TRUE
$  killall Dock
This hides all closed apps from your Dock at all times.

Change permissions to a file so anyone can read and/or modify it:
$  sudo chmod 777 <file path> 
( to allow access and read-only permissions, change the 777 to 644 )

Make the Dock slide more quickly: 
$  defaults write com.apple.dock autohide-delay -float 0 
$  killall Dock

Make your Mac Speak:  
$  say “<whatever you want the mac to speak>” 

Get rid of Dashboard completely:  
$  defaults write com.apple.dashboard mcx-disabled -boolean TRUE 
( can change it back by setting TRUE to FALSE )

Clear the window:  
$  clear 

Stress Test your Mac: 
$  yes 
( Cancel this by doing Ctrl+C )

View FileSystem usage:
$  sudo fs_usage
( Cancel this by doing Ctrl+C )

Get your external IP Address: 
$  curl ipecho.net/plain; echo 

Test your network connectivity: 
$  ping -c 10 www.apple.com 

Autocomplete Paths:  
when entering a command and you have a long path, you can simply start typing a few letters and enter TAB.  should see it either jump to the folder if only one exists matching it, or list the possible matches

See a list of all the commands you’ve entered:
$  history  



show all hidden files:  
$  defaults write com.apple.finder AppleShowAllFiles -bool TRUE
$  killall Finder
(  you can re-hide all your files, just change the TRUE to FALSE. )

Make holding down a key repeat characters:
$  defaults write -g ApplePressAndHoldEnabled -bool FALSE 
( you can undo the command by setting FALSE to TRUE )

List the contents of a folder (including sub-folders):
$  ls -R<the path of the folder> 



References used:
https://www.imore.com/fifteen-terminal-tricks-every-mac-user-should-know
https://www.macworld.co.uk/how-to/mac-software/mac-terminal-projects-tutorial-3613813/
https://computers.tutsplus.com/tutorials/40-terminal-tips-and-tricks-you-never-thought-you-needed--mac-51192






Non shell related shortcuts etc.:

Immediately lock your Mac:
Ctrl+Cmd+Q  


