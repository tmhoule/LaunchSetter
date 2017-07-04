# LaunchSetter
Set LaunchServices filetypes

LaunchSetter is a command line tool to define what program should be used for different URL handlers.  For example, what application should open http or mailto links. It should be run as the user account that needs the URL mapped.  Do NOT run it as root.  If running via a management tool (such as JAMF), you'll need to craete a LaunchAgent to execute the command.  

# Get Usage: 

     LaunchSetter get https

Will return the application the OS will use for https links.  

# Set Usage:

     LaunchSetter set mailto com.apple.Mail

Will map mailto links to the application Apple Mail.  

To find the application Bundle ID required by LaunchSetter, type the following in Terminal:
     
     
     defaults read /Applications/Mail.app/Contents/Info.plist CFBundleIdentifier
     
