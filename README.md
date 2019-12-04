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

_Note: these activities show up when visibility is set to ‘true’ for all items in the activity, see noCL branch applet_
<br/>

These conditioned items work fine:<br/>

| itemId | activityId | question |
| ------------- | ------------- | ---------------------- |
| Context1a  | context_of_assessment | When did you take it off and put it back on? | 
| Thoughts2a | positive_and_negative_thoughts | Were these thoughts about:
| Thoughts2b | positive_and_negative_thoughts | How severe or disturbing would you say these thoughts were?
| Event4a | life_events | To what degree did this other event have a positive impact on you? |
| Event4b | life_events | To what degree did this other event have a negative impact on you? |
| Pain1a | physical_pain | Where are you having pain? |
| Pain1b  | physical_pain | How severe is your pain right now? |
| Pain2a | physical_pain  | Where did this pain occur |
| Pain2b | physical_pain  | How severe was the pain you experienced since the last questionnaire |
| Activity1a | physical_activity  | About how long was your nap or rest? |
| Activity1a | physical_activity  | Did you actually fall asleep during the nap or rest? |




