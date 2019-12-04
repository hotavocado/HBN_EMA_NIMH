# HBN_EMA_NIMH
A test repo for HBN EMA applet with NIMH content.
 
<br>

There are three applets in this repo:

### 1. master branch applet

+ This applet was converted using data_dic_noTR.csv in the master branch. All single time selection questions were replaced with dropdowns
+ This applet has the ideal conditional logic in the activity_schema files
+ However, this causes a few activities to not display at all: morning_sleep_and_behavior, intake, headache

<br>

Preview the applet here:<br/>
https://schema-ui.anisha.pizza/#/activities/12?url=https%3A%2F%2Fraw.githubusercontent.com%2Fhotavocado%2FHBN_EMA_NIMH%2Fmaster%2Fprotocols%2FEMA_HBN%2FEMA_HBN_schema



### 2. test1 branch applet

+ This applet was converted using data_dic_noTR.csv in the test1 branch
+ I played with the conditional logic a bit, this applet should hopefully give more information on why conditional logic work for certain items and not others<br/>

These activities don't load at all:<br/>

| activityId  | displayName |
| ------------- | ------------- |
| headache  | Headache |
| intake  | Food and drinks  |

