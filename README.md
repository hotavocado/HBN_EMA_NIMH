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

**These activities don't load at all:**<br/>

| activityId  | displayName | 
| ------------- | ------------- |
| headache  | Headache | 
| intake  | Food and drinks  |  

visibility object for headache_schema:<br/>

   `"visibility": {
            "Headache1": true,
            "Headache1a": "Headache1 == 1",
            "Headache2": true,
            "Headache2a": "Headache2 == 0",
            "Headache2b": "Headache2 == 1",
            "Headache2d": "Headache2 == 1",
            "Headache2e": "Headache2 == 1",
            "Headache2f": "Headache2 == 1",
            "Headache2fa": "Headache2 == 1",
            "Headache2g": "Headache2 == 1",
            "Headache2h": "Headache2 == 1",
            "Headache2i": "Headache2 == 1",
            "Headache2j": "Headache2 == 1",
            "Headache2k": "Headache2 == 1",
            "Headache2l": "Headache2 == 1",
            "Headache2m": "Headache2 == 1",
            "Headache2n": "Headache2 == 1",
            "Headache2na": true,
            "Headache2o": "Headache2 == 1",
            "Headache2oa": "Headache2o == 1",
            "Headache2p": "Headache2 == 1",
            "Headache2pa": "Headache2p == 1",
            "Headache2q": "Headache2 == 1",
            "Headache2r": "Headache2 == 1"
        }`

_Note: these activities show up when visibility is set to ‘true’ for all items in the activity, see noCL branch applet_
<br/>

**These conditional logic items work fine:**<br/>

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

<br/>

**These conditional logic items work some of the time, depending on which choice is selected from the question upstream:**<br/>

| itemId | activityId | question |
| ------------- | ------------- | ---------------------- |
| Activity2a  | physical_activity  | When did you take it off and put it back on? | 
| Activity2b | physical_activity  | Were these thoughts about:
| Activity2c | physical_activity  | How severe or disturbing would you say these thoughts were?
| Activity2d | physical_activity  | To what degree did this other event have a positive impact on you? |
| Activity2e | physical_activity  | To what degree did this other event have a negative impact on you? |
| Activity2f | physical_activity  | Where are you having pain? |
| Daily_b3a | daily_events_and_overall_health_b  | How much did your allergies bother you today? |
| Daily_b3b | daily_events_and_overall_health_b  | How much did your asthma or respiratory difficulties bother you today? |
| Daily_b3c | daily_events_and_overall_health_b  | Which (if any) of the following gastro-intestinal/stomach symptoms did you have today? |
| Daily_b3d | daily_events_and_overall_health_b  | How much did this (or these) gastro-intestinal/stomach symptom(s) bother you today? |
| Daily_b3e  | daily_events_and_overall_health_b  | How much did your muscle/joint pain bother you today? |
| Daily_b3f | daily_events_and_overall_health_b  | How much did your heart racing or pounding bother you today? |
| Daily_b3g | daily_events_and_overall_health_b  | Did these feelings occur in a particular situation (in a bus, in hot weather, or other condition?) |
| Daily_b3h | daily_events_and_overall_health_b  | Did you actually faint today? |



