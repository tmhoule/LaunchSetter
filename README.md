# LaunchSetter
Set LaunchServices filetypes

LaunchSetter is a command line tool to define what program should be used for different URL handlers.  For example, what application should open http or mailto links. It should be run as the user account that needs the URL mapped.  Do NOT run it as root.  If running via a management tool (such as JAMF), you'll need to craete a LaunchAgent to execute the command.  

![alt text](https://github.com/tmhoule/LaunchSetter/blob/master/ScreenShot1.png)

# Get Usage: 

     LaunchSetter get https

Will return the application the OS will use for https links.  

# Set Usage:

     LaunchSetter set mailto com.apple.Mail

Will map mailto links to the application Apple Mail.  

To find the application Bundle ID required by LaunchSetter, type the following in Terminal:
     
     
     defaults read /Applications/Mail.app/Contents/Info.plist CFBundleIdentifier
     
# Installing

Download LaunchSetter from the Repo and copy it somewhere useful like /usr/local/bin.  You'll need to make it executable so run the following command.

    chmod +x /path/to/LaunchSetter
    
Or you can compile it yourself.

