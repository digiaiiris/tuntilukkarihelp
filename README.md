# Introduction

Soon you will be enjoying the most efficient way of recording day's work entries into Workday. This tool is designed so that you could spend as little time as possible using it!

On purpose, work entries can be entered only for today. It is meant that you will record work entries at the end of every day — although you can see your entries straight also throughout the whole day.

Work entry recording is **description based**. In other words, you first tell what you have been up to and then the tool assists in choosing the correct project task to record the work to.

There are multiple ways in which you're helped to record day's work efficiently:

 1. Events from your Outlook calendar are provided as suggestions for work entries. If the events contain information about Workday project tasks (see details below) your only job is to accept the suggestions and you're done with them. 
 2. Recent Workday work entries are used to auto-fill project tasks for calendar events even if the events themselves do not contain project task information. The most recent work entry with a similar description (event subject) yields the suggested project task.
 3. Magic wand button allows you to select recent work entries as templates for the new work entries. If you have been doing the same things as yesterday, just click and enter the hours you spent for them today.
 4. A powerful search engine makes it easy to find the correct project task using one or more terms (words or parts of words) that occur in the task name.
 5. Work entries are saved in the background while you can continue entering new ones. No need to wait for anything.
 6. You don't need to fear forgetting to submit the work entries because it's taken care of automatically.
 7. You can easily see all the entries you have recorded for today and modify them if need be.
 8. The hour balance before today is shown alongside with today's total hours and the resulting current balance.

# Installation and Configuration

## Requirements
Tuntilukkari is used with a web browser. The application must be configured every time the user starts it on a new computer (or in incognito window). That is because the application stores user-specific data only in the storage of the user's browser. 

Currently, only Chrome browser is supported. This will change once Workday integration will be possible with another API than the one currently used.

## Chrome Extension Installation

The current Workday integration requires a custom extension installed on Chrome browser.
(In the future, integration will be updated to use a different API that does not need extensions.)

To install the extension:

1. Download the [extension](https://d2sbbz5gutol4d.cloudfront.net/extension.zip)
2. Extract `extension.zip` anywhere on your computer (just a temporary place, can be eg. under `Downloads` folder)
3. Open `chrome://extensions/` url on a Chrome tab (Three dots on the top right hand corner -> More Tools -> Extensions)
4. Toggle `Developer mode` **on** in the top right corner of the extensions page
5. Click `Load unpacked` and select `workday-integration-chrome-plugin` folder from where you unzipped the extension

## Authentication

The user will be prompted to authenticate using corporate credentials. Authentication allows the application to access user's calendar and make work entry suggestions based on today's events.

## Workday Window

Workday must be opened on another window/tab of the browser. Actually, it is enough to just briefly open Workday and then close it. That enables Tuntilukkari to use Workday's user session to access Workday APIs.

Tuntilukkari will prompt the user if the Workday session is going to expire and you need to open Workday again on another window.

# Usage and Features

## Hour Balances

![Hour balances screenshot](hourbalances.png)

In the top bar, three numbers are indicated concerning the hour balances:

 1. Total number of hours entered so far for today. This includes entries that are just being saved into Workday. Suggestions are not included.
 2. Hour balance before today, corresponding to the balance shown by `Time Off Balance`report for yesterday
 3. Current hour balance considering hour balance before today, the required work hours for today's and the total number of hours (1) entered so far. 

## Entering new Work Entry

![Enter new entry screenshot](enternewentry.png)

With this functionality, you can enter new work entries manually if the suggestions (see below) do not cover all the day's activities.

 1. Magic wand button opens a dialog where you can select recent activity as a tempate for the new work entry (see [below](#magic-wand-dialog-using-recent-activity-as-template) for more details).
 2. In the description field, you type in what you've been doing. This will be printed in the invoice sent to the customer, alongside with the project task. Often this is the same as a ticket number (eg. in Jira) or a calendar event subject (in which case you won't enter it manually here but you suggestions further below).
> Note that you can enter long and multiline text into the description field. After entering a long text, the text input will collapse and you will be indicated by an ellipsis (…) that some part of the text is not visible.
 4. Number of hours you've been working on the subject. The hours can be entered in 0.5 hours (30 minutes) precision.
 5. Selection of the project task that the work is targeted to (see below for more details on selecting the task). The project task will determine cost center, billing rate, etc.

The work entry will be saved automatically after you have entered data to all the fields. The recorded work entry moves to today's work entries and you may continue to enter another work entry right away.

> Pro tip: You can use `Tab` and `Shift+Tab` to move between fields quickly.

One word of caution: If you find yourself usually entering work entries manually to all the fields (description, hours, project task) you should probably either adopt other features of Tuntilukkari as well or change your whole way of organizing your time at work (some more about this further below).

### Magic Wand Dialog (Using Recent Activity as Template)

![Magic wand dialog screenshot](magicwanddialog.png)

The dialog shows recent activity that can be selected as a template for the new work entry.

 1. You can search recent activity using one or more terms (words or parts of words) that occur in the recent activity. For example, "Design act" matches "PROJ-123 **Design** a new way for users to inter**act** with calibration management".
 2. Workday work entries for the last 10 weeks are shown here. The list shows the descriptions of the work entries. A tooltip for each entry shows the latest entry date and the project task used. Selecting a recent Workday work entry preselects work description and project tasks fields, allowing you to type in the hours and move on to the next work entry.

## Project Task Selection

![Project task selection screenshot](projecttaskselection.png)

Project task is selected from a dropdown that shows all the available project tasks for the current user today.

 1. You can search project tasks using one or more terms (words or parts of words) that occur in the recent activity. For example, "Design act" matches "PROJ-123 **Design** a new way for users to inter**act** with calibration management".
 2. Project task is selected from the dropdown list.

> Pro tip: You can move from the search field to the list by hitting `Tab`. Then, you can use arrow keys to navigate and `Enter` to select the item in the list.



# Tips for Managing your Time at Work


# Development Roadmap


## Jira Integration Configuration

In the future v4 there will be Jira integration that allows the user to select recent Jira activity as work entry templates. Also, if Jira time tracking is used it will be integrated in a mutual way to further ease work entry recording and to enable overall work hour visibility at Jira side.
