# Fully-Fit-PennApps-Fall2018

## Inspiration

We noticed that individual have difficulty achieving their fitness goals due to external factors such as work and sleep patterns. As a result, many fitness applications do not provide a realistic time frame for achieving said goal. We felt that having an application that customizes different fitness goals everyday to fit the individuals work schedule and sleep pattern from the night prior. This would be compared to their final goal and predict an estimate of when the user is able to achieve it. 

## What it does

FullyFit uses both Fitbit and Muse API to get fitness and brain-waves (EEG data). Many features extracted from the data include steps taken, calories burnt, heart-rate, sleep and floors climbed each minute as well as each day. Also, data from Google calendar is extracted indicating the duration for which the user will be busy throughout the day. On the mental health side, FullyFit tracks brain wave activity via a Muse headband, allowing the app to adjust its exercise reminders based on mental stress and thinking. 

## How we built it
We used machine learning to predict if the user is able to meet his/her step or calories burned goal. We scikit-learn machine learning library to test several algorithms like Decision Trees, Logistic Regression, Random Forest and Bagging Ensemble methods. Even though we got higher accuracy with both Random Forest and Bagging Ensemble methods, we used the Decision Trees for predicting if the user meets his daily fitness goals. Decision Trees ended up being really quick and also reasonably accurate for implementation.  

## Challenges we ran into
There were some issues with the Fitbit api getting and handling intraday data for more than a month, so for demonstration purposes we analyzed only a months data. 

The FullyFit is more accurate if the user has his work schedule posted in advance. This helps it better predict if the user would be able to meet their goal or not and notify them with suggestions. 
## Things we learned
• We learned a lot about the different channels of signaling from the brain. Specifically: Delta waves which are most present during sleep.
Theta waves which are associated with sleep, very deep relaxation, and visualization. Alpha waves which occur when relaxed and calm. Beta waves which occur when, for example, actively thinking or problem-solving. Gamma waves which occur when involved in higher mental activity and consolidation of information.
• Our brainwave EEG API wrapper relied on old legacy Objective-C code that we had to interpret and make edits to.

• Interacting the Fitbit API
## Accomplishments that we're proud of
• Being able to implement both Fitbit and Muse API's in our application. 
• Getting a high prediction accuracy with Bagging ensemble methods (96.5%), Random Forest (89%) and Decision Trees (84%)

## What's next for FullyFit
We would like to analyze much more data that we did now as well as optimizing our algorithms on many users. Currently using the user's calendar we only use the duration of busy hours during as a feature in training our machine learning models. We would like to build on this and make our system smarter by also taking in account the spread of the events. For example if the person is busy with work later in the day, it can compensate. We also like to expand upon the application of Muse as a mental health guide.

