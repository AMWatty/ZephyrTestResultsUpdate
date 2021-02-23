---
What is it?
This is a plugin to update test results in Jira in Zephyr plugin. It supports any automation framework. 

Why should I make it?
This plugin helps to fater update of test results. 

Who should make it?
Any one who is using Zephyr Plugin in Jira can use this plugin to update test results.


When should I make it?
This plugin we should use along with our automation script. We can also use to update test results 

Where should I put it?
Any automation farmework can use this. We can also use this plugin to update standalone

How should I make it?

[if testcases inside folder]
zephyr = ZephyrTestUpdate(<JiraServerUrl>, <USERNAME>, <PASSWORD>, <JIRA_PROJECT>, <VERSION>, <CYCLE_NAME>, <FOLDER_NAME>)
[if testcases inside cycle]
zephyr = ZephyrTestUpdate(<JiraServerUrl>, <USERNAME>, <PASSWORD>, <JIRA_PROJECT>, <VERSION>, <CYCLE_NAME>)
zephyr.createTestCycle(<CYCLE_NAME>, <startdate>, <enddate>) [dates should be in mm/dd/yy]
zephyr.Create_Folder_under_cycle(<CYCLE_NAME>, <FOLDER_NAME>)
zephyr.AddTestCasesToCycle(<TEST-CASE-LABEL>, <CYCLE_NAME>, <FOLDER_NAME>)
zephyr.updateExecution(<JIRA-ISSUE-KEY>, <STATUS>, <LOG-if-it has>)
zephyr.bulkUpdateCompleteFolder(<STATUS>) [this will update whole folder/cycle]
zephyr.bulkUpdateExecution(<STATUS>, <JIRA-ISSUE-KEY1>,  <JIRA-ISSUE-KEY2>,  <JIRA-ISSUE-KEY3>) [this will upadte status of multiple keys]

---

projects for inspiration
https://github.com/mattrixman/zestyr
