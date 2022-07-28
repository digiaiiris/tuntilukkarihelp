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

## Chrome Extension Installation

The current Workday integration requires a custom extension installed on Chrome.
(In the future, integration will be updated to use a different API that does not need extensions.)

To install the extension:

1. Download the [extension](https://d2sbbz5gutol4d.cloudfront.net/extension.zip)
2. Extract `extension.zip` anywhere on your computer (just a temporary place, can be eg. under Windows `Downloads` folder)
3. Open `chrome://extensions/` url on a Chrome tab (Three dots on the top right hand corner of Chrome -> More Tools -> Extensions)
4. Toggle `Developer mode` **on** in the top right corner of the extensions page
5. Click `Load unpacked` and select `workday-integration-chrome-plugin` folder from where you unzipped the extension

## Jira Integration Configuration (TBD)

In the future v4 there will be Jira integration that allows the user to select recent Jira activity as work entry templates. Also, if Jira time tracking is used it will be integrated in a mutual way to further ease work entry recording and to enable overall work hour visibility at Jira side.
