# WaterCooler
Connect with people around a virtual water cooler!
This PowerApp allows people to sign up, record their interests, and connect with others in 15 minute 1:1 meetings during an hour of their choice. This can be helpful when large teams work across locations or when everyone is working from home.

For an app overview, check https://youtu.be/tR4xK3hZYUg

## Included Files
The files included are:  
Water Cooler.msapp - The PowerApp template  
WaterCoolerSchedule_20200519201617 - The PowerAutomate template for the email

## SharePoint List
You will also need to create a SharePoint list and connect it to the PowerApp. I recommend naming the list 'Water Cooler'. When you select the Data Source, it will make it pick up the new list without modification.
Create the following columns in the SharePoint list:

1. Interests  
    Text field

2. Time  
    Choice field  
    Populate in hour increments (8-9AM, 9-10AM, etc)

3. Time Zone  
    Choice field  
    Populate it with relevant time zones (for example, in the US - EDT, MDT, CDT, PDT)
  
4. Created By  
This is a default column, so no need to create it, but you may want to add it to your View on the SharePoint list.

## Permissions on the SharePoint List
This is a critical step to keep people from overwriting others' information.  
Go to the SharePoint list.  
Go into the List Settings.  
Click Advanced Settings.  
Under Create and Edit access, be sure to select 'Create items and edit items that were created by the user'

## Import the PowerApp and PowerAutomate
Once the SharePoint list is created, import the files to create the PowerApp and PowerAutomate.

## Ways to Modify
If you want a truly random experience where you can't see names, go to the Browse Screen and remove the first field or set the Visible design property to 'false'.

## Note about calendar.help
This app uses calendar.help to automate the scheduling of meetings, which means each user MUST register for it to work. Users can register at https://calendar.help.

You can adjust the code in the PowerAutomate to simply send the message asking for a time if this is not an option.

## Sharing to Teams
If you share this app on a tab in Teams, you must be sure that the SharePoint list exists in that team and you share the app with an Office 365 Security Enabled group per this documentation: https://docs.microsoft.com/en-us/powerapps/maker/canvas-apps/share-app#share-an-app-with-office-365-groups

## Usage
The Splash Screen loads on a timer for 3 seconds. When the next screen appears, the user sees a list where employees can add themselves, search, or be connected with a random person.

This app works best if people populate their own data. Because this is a PowerApp, there is a list limit of 500 people that can be displayed. For more information on potentially increasing this to 2,000 people, check here: https://docs.microsoft.com/en-us/powerapps/maker/canvas-apps/delegation-overview#changing-the-limit. Note: I did not test this!

## Other Information
The Water Cooler icon used was made by Creaticca Creative Agency from https://www.flaticon.com
